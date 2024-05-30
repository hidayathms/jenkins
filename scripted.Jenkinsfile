node {
    stage ('Test') {
        print 'Hello World'
    }
    if (env.TAG_NAME == "") {
        stage ('Runs on Tag Name')
            print 'Runs on Tag'
        }
    else {
        stage ('Runs on Branch Name') {
            print 'Runs on Branc'
        }
    }

}