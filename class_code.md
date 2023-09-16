# class code
## example
```
#include <iostream>
using namespace std;

class student {
	unsigned short grade;
	unsigned int student_ID;
	const char* name;
public:
	student() {
		cout << "class가 생성되었지만 값이 초기화 되지 않았습니다. 기본 값이 입력됩니다." << endl;
		value_setting();
	}
	student(unsigned short grade) {
		cout << "class가 생성되었고 학년만 입력되었습니다. 남은 부분은 기본값으로 입력됩니다." << endl;
		value_setting(grade);
	}
	student(unsigned short grade, unsigned int ID) {
		cout << "class가 생성되었고 학년과 학번만 입력되었습니다. 남은 부분은 기본값으로 입력됩니다." << endl;
		value_setting(grade, ID);
	}
	student(unsigned short grade, unsigned int ID, const char* name) {
		cout << "class가 생성되고 모든 값이 입력되었습니다." << endl;
		value_setting(grade, ID, name);
	}

	~student() {
		cout << "class가 사라졌습니다." << endl;
	}

	void value_setting(unsigned short grade = 1, unsigned int ID = 20230000, const char* name = "홍길동") {
		grade = grade;
		student_ID = ID;
		this->name = name;
	}

	void value_print() {
		cout << "당신의 학년 : " << grade << endl;
		cout << "당신의 학번 : " << student_ID << endl;
		cout << "당신의 이름 : " << name << endl;
		cout << endl;
	}

};

int main()
{
	student S1;
	student S2(2);
	student S3(2, 20203495);
	student S4(2, 20203495, "송보현");

	cout << endl;

	cout << "매개변수 X" << endl;
	S1.value_print();
	cout << "매개변수 1" << endl;
	S2.value_print();
	cout << "매개변수 2" << endl;
	S3.value_print();
	cout << "매개변수 3" << endl;
	S4.value_print();
}
```
