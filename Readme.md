const fileContent = $json.content; // Current file content
const newTag = JSON.parse($node["AI Agent"].json.output).tag;

const updatedContent = fileContent.replace(
  /^(\s*tag:\s*).*/m,
  `$1${newTag}`
);

return [
  {
    json: {
      content: updatedContent
    }
  }
];