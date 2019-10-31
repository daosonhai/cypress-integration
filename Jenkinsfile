pipeline {
    agent any
    stages {
        stage('setup') {
        steps {
          bat label: 'installing npm package', script: 'npm install'    
        }
}

    stage('run tests') {
        when {
            branch 'development'
        }
        steps {
            bat label: 'executing all api tests', script: 'npx cypress run --record --spec "cypress/integration/examples/actions.spec.js" --key b96d19e1-021c-4921-a6ae-2c2a94303485'    
        }
    }
    }
}