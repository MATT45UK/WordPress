node {
    def app

    stage('Clone repository') {
        /* Let's make sure we have the repository cloned to our workspace */

        checkout scm
    }

    stage('Build image') {
        /* This builds the actual image; synonymous to
         * docker build on the command line */

        image = docker.build("ubuntu-wp")
    }

    stage('Test image') {
        /* Ideally, we would run a test framework against our image.
         * For this example, we're using a Volkswagen-type approach ;-) */

      /* image.inside {
       *     sh 'echo "Tests passed"'
       * } */
    }
    stage('Push to ECR') {
        docker.withRegistry('matt45uk/wp-ubuntu', 'dockerhub'){
            image.push "web"
        }
    }
}
