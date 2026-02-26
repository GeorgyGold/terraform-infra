def name = "Ijeoma"
def age = 30
def isEngineer = true

println "Hello World"
println "My name is $name"

def x = 10
def y = 5

println x + y
println x * y

def fruits = ["apple", "banana", "mango"]

println fruits[1]      // apple
println fruits.size()  // 3

def person = [
  name: "Ijeoma",
  role: "DevSecOps",
  experience: 8
]

println person.name
println person["role"] 

def score = 80

if (score >= 70) {
    println "Pass"
} else {
    println "Fail"
}
for (fruit in ["apple", "banana", "mango"]) {
    println fruit
} 

def i = 1

while (i <= 3) {
    println i
    i++
}
def greet(name) {
    return "Hello, $name"
}
println greet("ijeoma")
def add(a, b) {
    a + b 
}
def sayHello = { name -> 
    println "Hello $name"
}
sayHello("Ijeoma")
stage("Build") {
    steps {
        echo "Building..."
    }
} 

pipeline {
  agent any

  stages {
    stage("Hello") {
      steps {
        echo "Hello Jenkins"
      }
    }
  } 
}
 

pipeline {
  agent any   // Run on any available worker

  environment {
    APP_NAME = "myapp"   // global variable
  }

  stages {

    stage("Build") {
      steps {
        echo "Building $APP_NAME"
      }
    }

    stage("Test") {
      steps {
        script {
          def result = 10 + 5
          echo "Test result: ${result}"
        }
      }
    }

  }
}


def environment = "dev"

if (environment == "prod") {
    println "Deploying to Production"
} else {
    println "Deploying to Development"
} 

try {
    println "Deploying..."
    throw new Exception("Something failed")
} catch (Exception e) {
    println "Error: ${e.message}"
}

stage("Deploy") {
  steps {
    script {
      try {
        sh "exit 1"
      } catch (e) {
        echo "Deployment failed"
      }
    }
  }
}
