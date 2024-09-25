  # What is private.dev?
 
  private.dev aims to be an AI workflow for coding providing a code, coming up with test, running code against the tests and then repeating if needed until reaches a limit or the tests return successfully.
 
 # Agents
 
 The main workflow is composed by 5 agents that talk to each other before sending you an answer, those agents are:
 
 * **Meta agent:**  receives the app suggestion and description and make it clear and direct removing or clarifying bits as necessary
 * **Product Manager:**  receives the app description and expands on it, providing full specifications and requirements for the final product and also describes expected behavior.
 * **QA specialist**: should describe quality tests, specifications and the requirements for a suggested code by the user.
 * **QA developer**: receives the tests' description, specifications and requirements then figures out python tests based on it
 * **Developer:** receives the specification, description and requirements for the tool and the test schema and sends out python code, then it shall receive back tests results and return new code back
 * **Security analyst:** checks for malicious code and eternal loops, it also suggests best practices if necessary

 ![Diagram showing private.dev workflow. The process starts with a user prompt. The Meta Agent refines the prompt, and the Product Manager expands it into full app specifications. The QA Specialist defines test specifications, and the QA Developer generates Python test code. The Developer creates the app code, which is checked by the Security Specialist for safety. If the code is safe, tests are run. If the tests fail, the process loops back for improvements. Green lines show generated app code, purple lines show test code, red lines show test results, and blue lines show agent interactions. The process iterates until tests pass or a limit is reached.](/docs/images/private.dev-fluxogram.png)