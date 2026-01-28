**How to create your own MCP server**
- Creat a folder myFirstMCP
- stying at that folder execute
  - `uv init .`
  - `uv add fastmcp mcp`
- Create file myFirstServer.py with contin:
     ```
      from fastmcp import FastMCP

      mcp = FastMCP("Demo 🚀")

      @mcp.tool
      def add(a: int, b: int) -> int:
        """Add two numbers"""
        return a + b

      if __name__ == "__main__":
        mcp.run(transport="stdio")
       #mcp.run(transport="streamable-http")
     ```
- We can create client two ways:
- Create file client_mcp.py
  ```
  import asyncio

  from mcp import ClientSession
  from mcp.client.streamable_http import streamable_http_client


  async def main():
    url = "http://127.0.0.1:8000/mcp/"
    async with streamable_http_client(url) as (read, write, get_session_id):
        async with ClientSession(read, write) as session:
            print("Before initialize:", get_session_id())

            await session.initialize()

            sid = get_session_id()
            print("Session ID after initialize:", sid)

            result = await session.call_tool("add", {"a": 21, "b": 2})
            print("Server result:", result)
  if __name__ == "__main__":
    asyncio.run(main())
  ```
- or/and create file client_fastmcp.py
    ```
  import asyncio
  from fastmcp import Client

  async def main():
    async with Client("http://127.0.0.1:8000/mcp") as client:
        if client.is_connected:
            print("Connected to MCP server")

        # 🔍 List available tools
        tools = await client.list_tools()
        print("\n--- Available Tools ---")
        for t in tools:
            print(f"{t.name}: {t.description}")

         # 📡 Call the "add" tool
        response = await client.call_tool("add", {"a": 5, "b": 7})
        print("\n--- Tool Response ---")
        print("5 + 7 =", response)

  if __name__ == "__main__":
    asyncio.run(main())
  ```
 - run by `uv run  myFirstServer.py`
 - run by `uv run client_py`
 - run by `uv run clientfastmcp.py`

if __name__ == "__main__":
    asyncio.run(main())
