@@ -1,12 +1,10 @@
{
  "tasksRunnerOptions": {
    "default": {
      "runner": "nx/tasks-runners/default",
      "options": {
        "cacheableOperations": [
          "build",
          "prepare:dev",
          "prepare:lint"
          "build"
        ]
      }
    }
  },
  "targetDefaults": {
    "build": {
      "dependsOn": [
        "^build"
      ]
    },
    "build:docs": {
      "dependsOn": [
        "^build"
      ]
    },
    "dev": {
      "dependsOn": [
        "prepare:dev"
      ]
    },
    "lint": {
      "dependsOn": [
        "^prepare:test"
      ]
    },
    "test:unit": {
      "dependsOn": [
        "^prepare:test"
      ]
    }
  }
}
