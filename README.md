СТРУКТУРЫ
точки на плоскости 
struct point2
struct point2 
{
float x;
float y;
};
инициальзация
point2 point {0, 0};

обращение к полям через .
std::cout << point.x << point.y;
std::cin - также 

поля нужно именовать с большой буквы
Point2 point1 = point2;
пареллельный перенос координат

ССЫЛКИ

int main()
{
  int z = 0;
  int x = 13;
  
  z = x;
  не зависят друг от друга
  x = 123 // x == 123, z == 13
  z = 4 // x == 123, z == 4

амперсант 
int& y = x;

y += 10;
у ссылается на х поэтому изменится ячейка памяти х и изменится х
при изменение х меняется и у тк они являются неразрывной структурой

ссылки инициализируются при создании 

константная ссылка 
мы не имеенм права изменять внутренние поля

const student& ref = anna;
anna мы можем поменять,

struct Student
{
std::string Name;
std::string LastName;
std::vector<int> raitings;
};
int main ()
{
const Student anna = {
"anna"
"ivanova"
};
const Student& ref = anna;

защита от дуракак ( ни anna  ни ivanova нельзя менять )

for (int i : anna.raitings) =======                           одно и тоже (выполняют одно дейтсвие)
====== for (int i = 0; i < anna.raitings.size(); ++i)         способ пробежаться по всем ячейкам 
{
{std::cout << i << std::endl;
}

std::vector<Student> group = {};

for (Student s : group)
{
std::cout << s.Name << std::endl;
}
