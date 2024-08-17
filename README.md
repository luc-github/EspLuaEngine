# EspLuaEngine for ESP boards

Unleash the power of flexible scripting on your ESP32 with EspLuaEngine! This library brings the versatility of Lua 5.3.7 to ESP devices, enabling dynamic and adaptable IoT applications.

While primarily optimized for ESP32, EspLuaEngine is also compatible with ESP8266 and ESP8685 platforms, albeit with reduced performance. This cross-platform support allows you to leverage Lua scripting across a range of ESP microcontrollers.


## 🌟 Key Features

- **Highly Flexible**: Easily extend Lua with custom C functions and constants tailored to your project needs.
- **Resource-Efficient**: Optimized Lua 5.3.7 implementation designed for ESP32's constrained environment.
- **Arduino-Compatible**: Seamless integration with the Arduino framework for ESP32.
- **Customizable**: Add only the functionalities you need, keeping your project lean and efficient.

## 🚀 Quick Start

```cpp
#include "EspLuaEngine.h"

EspLuaEngine* lua;

void setup() {
  Serial.begin(115200);
  lua = new EspLuaEngine();
  
  // Register custom functions and constants
  lua->registerFunction("myCustomFunction", l_myCustomFunction);
  lua->registerConstant("MY_CONSTANT", 42);
  
  // Execute a Lua script
  lua->executeScript("print('Hello from ' .. _VERSION)");
}

void loop() {
  // Your Arduino loop code here
}
```

## 💡 Example Scripts

EspLuaEngine comes with several example scripts demonstrating its capabilities:

1. **HelloWorld**: A basic introduction to Lua scripting on ESP32.
2. **GPIO**: Demonstrates GPIO control using Lua scripts.
3. **Files**: Showcases file operations using the ESP32's file system.

Check out the `examples/` directory for the full scripts and more advanced use cases.

## 🔧 Customization

EspLuaEngine shines in its ability to adapt to your project's specific needs:

- **Add Custom Functions**: Extend Lua with C functions tailored to your hardware or application.
- **Define Project-Specific Constants**: Easily add constants that are relevant to your project.
- **Select Modules**: Include only the Lua modules you need, optimizing for size and performance.

## 📚 Documentation

For detailed API reference and customization guides, visit our [Wiki](https://github.com/yourusername/EspLuaEngine/wiki).

## 🤝 Contributing

We welcome contributions! Whether it's adding new features, improving documentation, or reporting issues, your input is valuable.

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Inspired by [ESP8266-Arduino-Lua](https://github.com/fdu/ESP8266-Arduino-Lua)
- Built on the robust foundation of [Lua 5.3.7](https://www.lua.org/)

---

Elevate your ESP32 projects with the flexibility of EspLuaEngine! 🚀✨