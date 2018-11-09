#include <stdio.h>
#include <stdlib.h>
#include <signal.h>
#include <unistd.h>

static void sighandler(int signo){
  if(signo == SIGINT){
    printf("Exiting\n");
    exit();
  }
}

int main(){
  signal(SIGINT,sighandler);
  signal(SIGUSR1,sighandler);
  while(1){
    printf("PID: %d\n",getpid());
  }
}
