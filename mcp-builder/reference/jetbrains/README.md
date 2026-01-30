# JetBrains / Junie MCP Reference

## Current Status

**Note:** As of this writing, there are no public APIs available for programmatic integration with Junie. Unlike the Anthropic SDK which provides direct API access for building MCP servers, JetBrains has not yet released public APIs for Junie integration.

## Available Interaction Methods

Currently, the only way to interact with Junie is through:

1. **Direct Commands** - Issue commands to Junie through the JetBrains IDE interface
2. **Skills** - Create and use Junie Skills (markdown-based instruction files in `.junie/skills/`)
3. **Natural Language** - Communicate with Junie using natural language within your JetBrains IDE

## JetBrains IDE Built-in MCP Server

JetBrains IDEs include their own built-in MCP server that Junie can interact with. This provides access to IDE tools and functionality directly through the MCP protocol.

**Important Considerations:**

- **Stability**: The built-in MCP server's stability is uncertain and may vary between IDE versions
- **Best Practice**: It is recommended to let Junie run IDE tools itself rather than attempting to invoke them programmatically. IDE tools accessed through Junie have been tested and approved by JetBrains, ensuring more reliable behavior
- **Tested Integration**: When Junie executes IDE operations, it uses pathways that JetBrains has validated, reducing the risk of unexpected behavior

## MCP Server Development for Junie

While Junie supports MCP (Model Context Protocol) servers, the development approach differs from Anthropic's SDK-based method:

- **No SDK Required** - Junie discovers and uses MCP servers without requiring an Anthropic-style SDK
- **Configuration-Based** - MCP servers are configured through JetBrains IDE settings
- **Standard MCP Protocol** - Servers should follow the standard MCP protocol specification
- **Prefer Junie-Driven Execution** - Rather than building custom tooling, consider letting Junie use the IDE's built-in capabilities which have been tested by JetBrains

## Future Updates

This directory will be updated when JetBrains releases:

- Public APIs for Junie integration
- Official SDK or client libraries
- Programmatic access methods for building Junie-integrated applications

## Resources

- [Junie Overview](https://www.jetbrains.com/junie/) - Official Junie product page
- [JetBrains AI Documentation](https://www.jetbrains.com/help/idea/ai-assistant.html) - AI features in JetBrains IDEs
- [MCP Specification](https://modelcontextprotocol.io/) - Model Context Protocol documentation

## See Also

- [../anthropic/](../anthropic/) - Reference materials for Anthropic/Claude MCP development (for comparison)
