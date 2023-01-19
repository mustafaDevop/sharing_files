## Exercise: Sharing Files

Create and share files between jobs in a workflow.

Instructions:

* Use the repository and Circle CI config file from previous exercises or create a new one.

* If you're reusing your repository, you can remove the hello world jobs we added from previous exercises.

* Add a job named save_hello_world_output. It should look very close to the print_hello job from the previous exercise with one small exception. We want to output "hello world" to a file called output.txt. If you're not sure how to do this, the bash statement would be something like echo "text to output here" > output.txt.

* Add a persist_to_workspace block (documentation)[https://circleci.com/docs/configuration-reference/#persist_to_workspace] to that job and reference output.txt so that it gets saved to the "workspace" (making it available to other jobs).

* Add another job named print_output_file.

* In this job, add a attach_workspace block (documentation)[https://circleci.com/docs/configuration-reference/#persist_to_workspace] (much like attaching a hard drive).

* In this job, also run a bash command that prints the contents of output.txt. For example: cat output.txt.
