node {
  checkout scm

  stage 'Deploy application release'
  writeFile file: 'extras.json', text: "{'image_tag':'${IMAGE_TAG}'}"
  sh 'ansible-playbook site.yml -e "@extras.json"'
}
