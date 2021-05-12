node {
    checkout scm

    docker.withRegistry('https://hub.docker.com', '81d97687-7e53-4115-a641-c766ad7c61eb') {

        def customImage = docker.build("my-image:${env.BUILD_ID}")

        /* Push the container to the custom Registry */
        customImage.push()
    }
}