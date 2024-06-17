Retail Mobile App - Architectural Decision Record (ADR)

Project Overview:
This project involves the development of a mobile app for a retail company. The app enables customers to browse and purchase products, check order history, track deliveries, and participate in a loyalty program. The app also supports offline mode, push notifications, payment gateways, user behavior tracking, image optimization, and internationalization.

Group Members:

	• Anamika Rijal
	• Kulbir Kaur
 	• Sahilpreet Singh
	• Supreet Dhillon
	• Vraj Patel

Architectural Decision Record (ADR):
The Architectural Decision Record (ADR) outlines the key decisions made during the development of the retail mobile app. It includes the rationale behind each decision and its consequences.

ADR: Development and Technology Stack Decisions

Date: 16th May 2024

Context and Problem Statement:
Our team is developing a mobile app for a retail company. The app enables customers to browse and purchase products, check order history, track deliveries, and participate in a loyalty program. The app also supports offline mode, push notifications, payment gateways, user behavior tracking, image optimization, and internationalization. We need to make informed decisions regarding the app's architecture, development approach, and technology stack to meet these requirements.

▪ Decision Drivers:

	  • Performance and user experience
	  • Development time and cost
	  • Cross-platform compatibility
	  • Offline capability
	  • Security and scalability
	  • Integration with third-party services
	  • User privacy and compliance with regulations

▪ Considered Options:

	  1 Native App (Separate iOS and Android Development)
	  2 Web App (Responsive Web Design)
	  3 Hybrid App


▪ Decision Outcome:
We chose to develop a Hybrid App using Flutter, and made the following decisions regarding the technology stack:

1. Development Approach:

   ◦ Decision: Hybrid App using Flutter

	◦ Status: Accepted

	◦ Consequences:

       ▪ Positive: Single codebase saves money and maintenance efforts, near-native performance, and robust UI components.
       ▪ Negative: Reduced ability to take advantage of platform-specific features, slightly larger app size compared to true native apps.

	◦ Rationale: Efficiency of development and performance, robust support for both iOS and Android, and native-like user experience.

2. UI Framework:

   ◦ Decision: Flutter

	◦ Status: Accepted

	◦ Consequences:

  		▪ Positive: Smooth animations, high performance, single code base for iOS, Android, and web, extensive library of widgets, and rapid iteration times via Hot Reload.
  		▪ Negative: Smaller framework and community, bulkier app size, lack of third-party library support.
	
	◦ Rationale: Pre-designed widgets resembling native interfaces, excellent performance, and comprehensive documentation.

3. Backend Language:

	◦ Decision: Node.js with Express.js

	◦ Status: Accepted

	◦ Consequences:

		 ▪ Positive: Efficient for I/O operations, JavaScript usage on both client and server sides, several libraries from npm, manages multiple connections simultaneously, simplifies maintenance and development, and increases development speed.
		 ▪ Negative: Asynchronous programming can be complicated and may require a learning curve for developers unfamiliar with JavaScript or Node.js.
   
	◦ Rationale: Wide ecosystem, real-time performance, and scalable RESTful APIs connecting the backend to the Flutter front-end.

4. Permissions:
   
	◦ Decision: Internet access, push notifications, location services, storage, camera, and background data synchronization
	
	◦ Status: Accepted
	
	◦ Consequences:
	
		  ▪ Positive: Comprehensive permissions improve user experience.
		  ▪ Negative: Managing several permissions might complicate development and cause privacy concerns.
	 
	◦ Rationale: Necessary for offline mode, notifications, and picture uploads. Users will be clearly informed about the purpose of each permission.

5. Data Storage:
   
	◦ Decision: Local storage using SQLite for offline mode and Firebase for remote storage
	
	◦ Status: Accepted
	
	◦ Consequences:
	
		  ▪ Positive: SQLite ensures reliable local data storage and offline functionality, Firebase provides real-time data synchronization and scalable cloud storage.
		  ▪ Negative: Careful synchronization logic is needed when using multiple storage options.
	 
	◦ Rationale: SQLite is lightweight and effective for offline applications, while Firebase's real-time synchronization is crucial for data syncing when an internet connection is available.

6. Additional Frameworks and Technology Stacks:
   
	◦ Decision:
	
	  	▪ Push Notifications: Firebase Cloud Messaging (FCM)
	  	▪ Payment Gateway: Stripe
	  	▪ Analytics: Google Analytics for Firebase
	  	▪ Image Optimization: Cloudinary
	  	▪ Localization: Flutter Intl plugin
	  	▪ API Testing: Postman
	
	◦ Status: Accepted
	
	◦ Consequences:
	
		  ▪ Positive: Industry-standard solutions with ample documentation and support, security and reliability, seamless integration with Flutter and Node.js backend, efficient API testing and debugging.
		  ▪ Negative: Dependency management and potential vendor lock-in.
	 
	◦ Rationale: FCM provides reliable push notifications, Stripe offers robust security and ease of integration, Google Analytics for Firebase delivers comprehensive insights, Cloudinary handles image storage and optimization effectively, Flutter Intl plugin simplifies internationalization, and Postman ensures thorough API testing and debugging.
