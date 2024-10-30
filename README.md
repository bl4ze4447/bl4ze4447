## Welcome to my profile
```cpp
#include <iomanip>
#include <iostream>
#include <vector>

struct Skill {
    std::string name;
    float       rating;
};

class programmer {
public:
    programmer(const std::string &name, const std::string &preferred_lang, const std::vector<Skill> &skills) {
        _name               = name;
        _preferred_lang     = preferred_lang;
        _skills             = skills;
    }

    void greet_visitor() const {
        std::cout <<    "Hey, my name is " << _name << "!\n"
                        "I love programming in " << _preferred_lang << " and I also love petting my dog!\n\n"
                        "I also love: \n";

        for (const auto& [name, rating] : _skills) {
            std::cout << "> " << std::left << std::setw(6) << name
                      << std::right << std::setw(4) << " (" << rating << "/10)\n";
        }
    }
private:
    std::string                 _name;
    std::string                 _preferred_lang;
    std::vector<Skill>          _skills;
};

int main(int argc, char * argv[]) {
    const auto me = programmer("bl4ze", "C++",{
            {"Rust", 7},
            {"C", 8.5f},
            {"C#", 7},
            {"MySQL", 7},
            {"ECDL", 10}
    });

    me.greet_visitor();

    return 0;
}
```
```powershell
./readme.exe bl4ze cpp
Hey, my name is bl4ze!
I love programming in C++ and I also love petting my dog!

I also love:
> Rust     (7/10)
> C        (8.5/10)
> C#       (7/10)
> MySQL    (7/10)
> ECDL     (10/10)
```
<!---
bl4ze4447/bl4ze4447 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
