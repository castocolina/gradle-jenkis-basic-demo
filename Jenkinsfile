// This shows a simple build wrapper example, using the Timestamper plugin.
node {
    // Adds timestamps to the output logged by steps inside the wrapper.
    timestamps {
        // Just some echoes to show the timestamps.
        stage "First echo"
        echo "Hey, look, I'm echoing with a timestamp!"

        stage "View current dir files"
        sh "ls -la"

        stage "View current dir recursive files"
        sh "ls -laR"

        stage "Load settings.gradle"
        // Now load 'externalCall.groovy'.
        def gSettings = load("settings.gradle")

        // A sleep to make sure we actually get a real difference!
        stage "Sleeping"
        sleep 3

        // And a final echo to show the time when we wrap up.
        stage "Second echo"
        echo "Wonder what time it is now?"
    }
}
