node {
    stage ('Test') {
        print 'Hello World'
    }
    if (env.TAG_NAME == "") {
        stage ('Todays Session')
            print 'Todays session is History'
        }
    else {
        stage ('Tommorows Session') {
            print 'Todays session is Maths'
        }
    }

}