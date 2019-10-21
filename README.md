#What have I learnt:
## Top level
1. `subprojects` are defined in `settings.gradle` using
`include 'sub-project-a'`
`include 'sub-project-b'`
2. define as many common things in top level `build.gradle` as possible
3. possible to apply dynamically some common things between `subprojects` using 
`configure(subprojects.findAll { it.name == 'greeter' || it.name == 'greeting-library'}) {...}`

## Sub-projects
1. Dependencies between `subprojects` are defined using
`dependencies {
   compile project(':greeting-library')
 }
`