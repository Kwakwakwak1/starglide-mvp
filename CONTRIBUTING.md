# Contributing to StarGlide MVP

Thank you for your interest in contributing to StarGlide MVP! We're excited to have you join our community of developers making spatial experiences more accessible.

This document provides guidelines and instructions for contributing to this project.

## Table of Contents

- [Contributing to StarGlide MVP](#contributing-to-starglide-mvp)
  - [Table of Contents](#table-of-contents)
  - [Code of Conduct](#code-of-conduct)
  - [Getting Started](#getting-started)
  - [Development Workflow](#development-workflow)
  - [Pull Request Process](#pull-request-process)
  - [Coding Standards](#coding-standards)
  - [Performance Considerations](#performance-considerations)
  - [Communication](#communication)
  - [License](#license)

## Code of Conduct

This project adheres to our [Code of Conduct](CODE_OF_CONDUCT.md). By participating, you are expected to uphold this code. Please report unacceptable behavior to [project-maintainers@example.com](mailto:project-maintainers@example.com).

## Getting Started

1. **Fork the Repository**
   - Create your own fork of the repo on GitHub

2. **Clone Your Fork**
   ```bash
   git clone https://github.com/YOUR-USERNAME/starglide-mvp.git
   cd starglide-mvp
   ```

3. **Set Up Development Environment**
   ```bash
   npm install
   ```

4. **Create a Branch**
   ```bash
   git checkout -b feature/your-feature-name
   ```

## Development Workflow

1. **Make Your Changes**
   - Write code that follows our [coding standards](#coding-standards)
   - Add or update tests as necessary
   - Ensure your code meets performance requirements

2. **Test Your Changes**
   ```bash
   npm run test
   npm run lint
   ```

3. **Run the Development Server**
   ```bash
   npm run dev
   ```

4. **Test on Target Devices**
   - Test on Vision Pro if possible
   - Otherwise, test on supported browsers and devices

## Pull Request Process

1. **Update Documentation**
   - Add comments to your code where necessary
   - Update README.md if your changes affect usage or installation
   - Document any new features or changes to existing features

2. **Commit Your Changes**
   ```bash
   git commit -m "Description of the changes"
   ```

3. **Push to Your Fork**
   ```bash
   git push origin feature/your-feature-name
   ```

4. **Open a Pull Request**
   - Use a clear and descriptive title
   - Include a detailed description of the changes
   - Reference any related issues using the syntax `Fixes #123` or `Relates to #123`

5. **Code Review**
   - Wait for a review from maintainers
   - Address any requested changes
   - Once approved, your PR will be merged

## Coding Standards

- **JavaScript/Three.js**
  - Use ES6+ syntax
  - Follow the [Airbnb JavaScript Style Guide](https://github.com/airbnb/javascript)
  - Document functions and complex logic with JSDoc comments

- **Performance Optimization**
  - Optimize meshes and textures
  - Minimize draw calls
  - Use LOD (Level of Detail) when appropriate
  - Implement object pooling for frequently created/destroyed objects
  - Follow the [Performance Guidelines](README.md#-performance-guidelines)

- **XR Best Practices**
  - Maintain 72+ FPS at all times
  - Design interactions that work across multiple XR platforms
  - Consider accessibility in all UI decisions
  - Test hand tracking on real devices

## Performance Considerations

When contributing to StarGlide MVP, keep the following performance considerations in mind:

- **Asset Optimization**
  - Keep models under 20K triangles
  - Use compressed textures (basis, etc.)
  - Implement asset streaming for large environments

- **Render Pipeline**
  - Limit shader complexity
  - Batch similar materials
  - Use instancing for repeated geometries

- **Memory Management**
  - Dispose of unused Three.js objects properly
  - Avoid memory leaks in event listeners
  - Profile memory usage regularly

## Communication

- **Issues**
  - Use GitHub Issues for bug reports and feature requests
  - Be specific and include reproduction steps for bugs
  - For feature requests, explain the use case

- **Discussions**
  - Use GitHub Discussions for questions and broader topics
  - Join our [Discord server](https://discord.gg/example) for real-time discussion

## License

By contributing to StarGlide MVP, you agree that your contributions will be licensed under the project's [MIT License](LICENSE).

---

Thank you for contributing to make StarGlide MVP better! 