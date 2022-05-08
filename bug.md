amqp

org.springframework.amqp.AmqpConnectException: java.net.ConnectException: Connection refused: connect





config 8888

Fetching config from server at: http://localhost:8888




http://localhost:1703/swagger-ui.html




@SpringBootApplication (exclude = {
//      排除数据源
        DataSourceAutoConfiguration.class,
//        禁止mongodb自动装配
        MongoAutoConfiguration.class,
//        禁止redis自动装配
        RedisAutoConfiguration.class,
        RedisRepositoriesAutoConfiguration.class,
//        禁止rabbitmq自动装配
        RabbitAutoConfiguration.class})
