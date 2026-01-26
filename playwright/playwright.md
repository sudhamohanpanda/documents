- for this I have created a project "TestAuto"
Reference: 

- https://cognizant.udemy.com/course/playwright-python-automation-testing-pytest/learn/lecture/46523023#overview

Why PlayWright?
- multi_language support: You can write testing code in different language like JavaScript, Python Java
- Web & API testing:
- Multi- Browser and OS compatibility
- Automatic Waiting Mechanism
- Inbuilt Logging and Screenshots

PlayWright vs selenium vs cypress
| Category | **Playwright** | **Selenium (WebDriver)** | **Cypress** |
|---|---|---|---|
| **Primary Use & Maturity** | Modern cross‑browser automation (launched 2020), fast adoption; includes @playwright/test runner. | Long‑standing, enterprise‑proven browser automation standard (since 2004). | Dev‑friendly E2E testing focused on web apps; strong interactive runner. |
| **Language Support** | JS/TS, **plus** Java, Python, C#. | Broad: Java, Python, C#, Ruby, JavaScript, etc. (official bindings). | JavaScript/TypeScript only. |
| **Browser Coverage** | Chromium, Firefox, **WebKit** (covers Chrome, Edge, Firefox, Safari engine). | All major browsers via native WebDriver drivers; standardized W3C protocol. | Chrome‑family, Firefox, **WebKit (Safari engine)** support (now available, historically experimental). |
| **Multi‑tab / Multi‑window** | Fully supported via multiple contexts/pages. | Supported by native browser drivers. | **Not** natively supported; typical workarounds (remove `target=_blank`, stub `window.open`). |
| **Speed & Stability** | Very fast; auto‑waiting and actionability checks reduce flakiness. | Reliable but can be slower due to WebDriver client–driver communication overhead; improved with Selenium 4 features. | Fast for front‑end flows; interactive runner gives quick feedback. |
| **Waiting / Synchronization** | Built‑in **auto‑wait** for visibility/stability/enabled state; retrying assertions. | Explicit waits & expected conditions; now adds BiDi/CDP hooks for richer sync/debug. | Automatic waits for commands/assertions; still single‑tab model. |
| **Parallelism & Scale** | Parallel by default; workers configurable; projects for multi‑browser; trace viewer. | Selenium Grid enables large distributed parallel runs; strong cloud/grid ecosystem. | Parallel runs supported via CI/cloud runners; less grid‑oriented than Selenium. |
| **Mobile / Safari Coverage** | WebKit gives **Safari** engine; device emulation presets (iPhone/Android). | Full desktop browsers + **Appium** ecosystem for native/hybrid mobile. | WebKit brings Safari‑engine coverage; more focused on desktop web flows. |
| **Advanced Features** | Network interception, multiple contexts, codegen, tracing/UI mode. | Selenium 4 adds **CDP** access + emerging **WebDriver BiDi** (event‑driven, cross‑browser). | Time‑travel UI, stubs/mocks; strong DX inside test runner. |
| **Ecosystem & Community** | Rapidly growing; official docs + cloud support (BrowserStack, etc.). | Very large, mature, with multi‑language support and vendor tools/clouds. | Strong community around JS tooling; lots of guides and CI examples. |
| **Typical Strengths** | Cross‑browser (incl. WebKit), fast, less flaky via auto‑wait; great for modern SPAs. | Best for **broad compatibility**, legacy apps, enterprise grids & multi‑language teams. | Best **developer experience** and rapid feedback for JS teams; simple setup. |
| **Typical Limitations** | Primarily web; mobile apps require other tools (e.g., Appium). | Higher setup complexity; potential flakiness if waits/timeouts not tuned. | Single‑tab architecture limits multi‑window flows; WebKit support may require extra setup. |
| **License** | Apache 2.0. | Apache 2.0. | MIT (runner) + OSS ecosystem (varies by plugins). *(General)* |

- Pi test is one of the testing framework which you need to know before you get started with playwright. Basically, playwright tests are built on Pi test framework.
- pytest serves as a testing framework that allow us to execute Playwrigte test using pytest-playwright plugin
  # Setup  PlayWright
  - Install Python
  - Install pytest by executing pip install -U pytest
  - Install playwright-pytest plugin by executing pip install -U pytest-playwright
  - Install required browser by playwright install
  - in intellij IDE make sure blue play button is showing before every test_anyName. if not install python plugin and restart.

  # scope of pytest fixture
  Fixture is reusable function. Not a test. it can define in each python file with annotation @pytest.fixture or in file conftest.py. It will first check with in file then conftest.py.
  By default scope is function
  - if scope="function" it will run before each test function 
  - if scope="module" it will run once per python file
  - if scope="session" it will execute once across your test.
  - To run every test file use command "pytest"
    pytest command execute all the files which file name start with test
  - pytest -s ... will show print statement also.
  - to run particualr file pytest testFileName
  - to run a particular test pytest testFileName::testName
  - @pytest.mark.skip use this to skip a test
  - to run with particular tag annoted with pytest.mark.tagName and execute pytest -m tagName
 
  - **Note that your test file name must start with "test" and your test method also must start with "test"**
  # Record and playback the tests in playwright with codegen tool
  - command:  playwright codegen base-url



