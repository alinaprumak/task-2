# task-2
#include <iostream>

int main() {
    int n, target;
    if (!(std::cin >> n >> target)) return 0;

    int left = 1;
    int right = n;
    int kroky = 0;

    while (left <= right) {
        int mid = (left + right) / 2;
        
        std::cout << mid << std::endl;
        kroky++;

        if (mid == target) {

            break; 
        } else if (mid < target) {
            left = mid + 1;
        } else {
            right = mid - 1;
        }
    }
    
    std::cout << "kroky: " << kroky << std::endl;

    return 0;
}
