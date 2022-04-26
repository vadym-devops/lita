node {
    stage('Build') {
        try {
            echo 'Hello World'
        } catch (err) {
            // CHANGE_ID is set only for pull requests, so it is safe to access the pullRequest global variable
            if (env.CHANGE_ID) {
                pullRequest.addLabel('Build Failed')
            }
            throw err
        }
    }
}
