reference: https://cognizant.udemy.com/course/the-complete-agentic-ai-engineering-course/learn/lecture/49770319#overview by Ed Donner

 49. Crew AI
     - Crew AI Enterprise: A multi agents platform for deploying, running and monitoring Agentic AI.
     - Crew AI UI Studio: A no code or low code product for creating multi agent solutions.
     - Crew AI Open source Framework: Orchestrate hight perfomance AI agents with easy and scale.
     - Crew AI Framework come with two flavor :
    <img width="422" height="461" alt="image" src="https://github.com/user-attachments/assets/66e63c86-a1f5-4c30-b29a-c348fb63261b" />
 51. Core Concept
     - Agent: An autonomous unit, with an LLM, a role, a goal, a backstory, memory, tools
     - Task: A specific assignment can be carried out, with a description, expected output an agent.
     - Crew: A team of Agents and Tasksl either:
          - sequential: run tasks in order they define
          - Hierarchical: use a manager LLM to assign
52. CrewAI use super simple LightLLM under the hood to interface with any LLM.
53. Install crewAI by executing command "uv tool install crewai"
54. Start crew project by executing "crewai create crew my_crew"
    <img width="647" height="743" alt="image" src="https://github.com/user-attachments/assets/37baa894-3fcc-4f8a-8415-d7765f28285a" />
    It will create a dummy project with dummy agent, task and crew with main.
55. To run crewAI project staying within project execute "crewai run"
56. 
