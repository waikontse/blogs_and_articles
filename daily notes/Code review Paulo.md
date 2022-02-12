# Source
[Code for Isaac test](https://github.com/prsouz/Tickets/blob/master/src/main/java/com/io/ticket/usecase/TicketGenerator.java)

# Red flags
1. src/main/java/com/io/ticket/usecase/TicketGenerator.java - abstract class with abstract method. Why not just an interface?
2. src/main/java/com/io/ticket/usecase/TicketGenerator.java - Is throwing generic exceptions. Why not custom exceptions?
3. src/main/java/com/io/ticket/models/TicketDataModel.java - Why is it annotated with @Component? It means it's a singleton which we can inject. Inject where? Could have used the lombok @Builder
4. src/main/java/com/io/ticket/ports/out/SenderSqsLambdaPort.java - The interface could have been better placed, for example in the usecase package. This is one of the strengths of hexagonal architecture. All dependencies point to your 'application'.
5. src/main/java/com/io/ticket/usecase/TicketProcessUseCaseImpl.java - should have been a package private class and let spring inject the correct implementation. Also a violation of hexagonal architecture. @Autowired members, which is not recommended anymore. Recommended way is via constructor. Package private members, should be private.