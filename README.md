# Welcome to my profile
```cpp
#include <iostream>

class programmer {
public:
    programmer() = default;
    programmer(const std::string &name, const std::string &preferred_lang) {
        _name = name;
        _preferred_lang = preferred_lang;
    }

    void greet_visitor() const {
        std::cout << "Hey, my name is " << _name << "!\n"
                    "I love programming in " << _preferred_lang << " and petting my dog daily!\n";
    }

    static void invalid() {
        std::cout << "Well, it sure looks like I can't make a programmer out of you...\n";
    }
private:
    std::string _name;
    std::string _preferred_lang;
};

int main(int argc, char * argv[]) {
    if (argc != 3) {
        programmer::invalid();
        return 1;
    }

    const auto me = programmer(argv[1], argv[2]);
    me.greet_visitor();

    return 0;
}
```
```powershell
./readme.exe bl4ze cpp
```
<!---
bl4ze4447/bl4ze4447 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
