# pulumi-language-ai

This is an experimental Pulumi language host that lets you declare cloud resources in natural language.

Just download a release for your operating system and architecture, put it on your path, and choose `"ai"`
as your runtime in your `Pulumi.yaml` file:

```yaml
name: my-project
runtime: ai
```

For instance, here is a sample program:

```
An AWS EC2 instance running a Python web server.

It accepts traffic over the Internet on port 80 and simply responds "Hello, World."

Capture and export its auto-assigned IP address and DNS name.
```

Save this to a file with a `pai` extension (`pai` = Pulumi AI) and run any Pulumi commands, like `pulumi up`
or `pulumi watch`, and it will use an LLM to generate the cloud infrastructure from your prompt.

> Warning: cloud infrastructure isn't free; always check that the LLM is doing what you expect.
