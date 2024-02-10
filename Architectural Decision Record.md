Architectural Decision Record (ADR): Scenario 1

Native, Web or Hybrid App

Decision Title:
Type of Mobile App – Native, Web, or Hybrid

Context:
Determining whether the app will be better as an OS native application, a web application, or a hybrid application based upon practicality.

Options Considered:
•	App compatible with iOS only (iPhone and iPad).
•	App compatible with Android only (phones and tablets).
•	App functional as a website only.
•	App functional as a website and a mobile application for both iOS and Android.

Decision:
The decision is made to make a hybrid app which is compatible with iOS and Android as well as have a fully-functional web application version.

Rationale:
•	Cross-platform compatibility allowing maximum reach across multiple platforms.
•	All major market shares are covered ensuring diverse preferences.
•	Smooth user experience with compiled code to native components.
•	Lower development, testing, and maintenance costs.
•	Adaptable to evolving business requirements and scalable for future expansion.

Consequences:
•	Development time may be slightly longer compared to a pure web app due to the need for platform-specific adjustments and optimizations.
•	Unable to meet same level of performance as fully native apps.
•	Compatibility issues with certain device configurations, operating system versions, or hardware specifications.
•	Limited offline functionality, not living up to 100% potential.
Follow-Up Actions:
•	Include testing for various scenarios, such as offline mode, push notifications, payment transactions, and internationalization features.
•	Maintain up-to-date documentation for APIs, libraries, and third-party integrations used in the app to ensure clarity and consistency in development.
•	Implement optimization techniques to enhance the app's performance, such as minimizing network requests, optimizing image loading, and improving rendering speed.
























UI Framework

Decision Title:
UI Framework Selection

Context:
Selecting appropriate graphical user interface to satisfy all user specified needs.

Options Considered:
•	Top navigation bar allowing switching between sections.
•	Scrollable sections to show through categories.
•	Navigation bar at bottom, search bar, and options to view and modify order on top while displaying contents in the middle screen by categories

Decision:
The decision is made to categorise everything by the category they are sold by, blended perfectly on the screen with correct positioning of the icons (view cart, see previous orders, view account, etc.) 

Rationale:
•	Single screen split into sections reducing unnecessary network requests.
•	Options to view/edit the order resulting in user satisfaction.
•	Similar UI on different devices result in cohesion across the app.
•	Allowing for branding and style adaptations to match the retail company's aesthetics.
•	Availability of similar pre-designed UI components and patterns, reducing design and development time.

Consequences:
•	Periodic adjustments to the app to comply with current retail store theme.
•	Visually appealing UI reflects positively on the brand, enhancing its reputation and credibility among users.
•	Intuitive navigation, clear visuals, and interactive elements encourage users to explore the app more deeply
•	Customizations while using pre-designed components may require additional effort and expertise.
•	Adding animations, transitions, and other interactive elements to enhance usability may impact app performance.

Follow-Up Actions:
•	Conduct regular reviews of the UI design and development process to identify areas of improvement and streamline workflows.
•	Utilize design systems or UI component libraries to standardize and modularize UI elements, reducing duplication of effort and promoting consistency.
•	Conduct thorough testing on a variety of devices and platforms to identify and address any compatibility issues early in the development process.






















Backend Language

Decision Title:
Selecting Backend Language

Context:
Deciding the appropriate programming language for developing the backend infrastructure of the mobile app.

Options Considered:
•	Traditional Server-Side Languages: Options such as Python, Java, Ruby, and PHP.
•	Modern Web Frameworks: Node.js.
•	Specialized Backend Frameworks: Frameworks like Django (Python), Spring Boot (Java), Ruby on Rails (Ruby), or Laravel (PHP).

Decision:
The decision is made to continue with Node.js for the backend development. 

Rationale:
•	Allows for server-side JavaScript execution.
•	Consistency in language across both frontend and backend components.
•	Availability of a wide range of modules and libraries for integrating with databases, authentication systems, and other third-party services.
•	Active community support ensures ongoing updates, security patches, and enhancements to the ecosystem.
•	Well-suited for handling I/O-bound tasks.

Consequences:
•	CPU-intensive tasks or scenarios requiring heavy computational processing.
•	Tedious debugging process and error handling logic.
•	Load balancing, and caching strategies may need to be implemented to distribute incoming requests effectively.

Follow-Up Actions:
•	Establish coding conventions and best practices for Node.js development to maintain consistency and readability across the backend codebase.
•	Regularly review and update npm dependencies to ensure compatibility and security.
•	Implement logging, monitoring, and error tracking mechanisms to detect and address issues in the production environment proactively.

























Permissions

Decision Title:
Permissions Management

Context:
Determining how the mobile app will handle permissions to access sensitive device features and data.

Options Considered:
•	Request all necessary permissions upfront during the app installation or onboarding process.
•	Prompt users to grant permissions as needed when certain features are accessed within the app.
•	Request only essential permissions initially and prompt for additional permissions gradually as users interact with advanced features.

Decision:
The decision is made to go with dynamic permissions, which means prompting users to grant permissions as needed. 

Rationale:
•	Enhance user privacy by only requesting access to sensitive resources when necessary.
•	Reducing the initial apprehension users may have about granting extensive permissions upfront.
•	Aligns with platform guidelines and best practices, providing a smoother user experience.
•	Users are more likely to understand why certain permissions are needed, fostering trust.
•	More room to handle scenarios where users deny certain permissions initially but may grant them later.

Consequences:
•	Careful planning to ensure permissions are requested at appropriate points.
•	Continuous user feedback to identify optimal moments to request permissions and minimize user friction.
•	Requesting permissions too frequently can lead to user frustration.
•	Impact user’s experience on the app due to constant interruptions.

Follow-Up Actions:
•	Thorough user testing to identify the most effective points in the app flow to request permissions.
•	Concise explanations for why each permission is required to build user trust and encourage permission granting.
•	Continuously monitor user feedback and app analytics to iteratively refine the permissions management strategy based on user behavior and preferences.






















Data Storage

Decision Title:
Solution for Data Storage

Context:
Determining the appropriate data storage solution for the mobile app, considering requirements such as offline mode support and data synchronization with the server.

Options Considered:
•	Store data locally on the device using built-in storage mechanisms.
•	Store data exclusively on remote servers managed by the retail company's backend infrastructure.
•	Implement a combination of local and cloud storage to support offline mode and data synchronization.

Decision:
The decision is made to opt the hybrid approach, which is combining the local and cloud storage facilities. 

Rationale:
•	Local storage provides offline support, allowing users to access essential features like browsing products and viewing order history even without an internet connection.
•	Cloud storage ensures data consistency and synchronization with the server when the app is online.
•	Seamless updates to order status and loyalty points.
•	Robust solution that balances offline functionality with real-time data synchronization.

Consequences:
•	Implementing a hybrid storage solution may introduce additional complexity to the app's architecture and data management logic.
•	Careful consideration is required to ensure data integrity and consistency between the local and cloud storage systems, especially during synchronization processes.
•	Dealing with sensitive customer information stored in both local and cloud environments.

Follow-Up Actions:
•	Conduct thorough testing to validate the functionality and performance of the hybrid storage solution across different usage scenarios and network conditions.
•	Monitor and analyze user feedback to identify any potential issues or areas for improvement related to data storage and synchronization.
•	Continuously evaluate and optimize the hybrid storage implementation to maintain scalability, reliability, and security as the app evolves and scales in usage.
