# Đệ quy

## Input - Output
Input: Một bài toán được phát biểu theo cách đệ quy hoặc được giải theo cách đệ quy.

Output: Kết quả của bài toán đó hoặc kết quả của các bài toán con được giải quyết trong quá trình giải bài toán gốc.

Trong các thuật toán đệ quy, input thường là một bài toán được phát biểu dưới dạng đệ quy, và output là kết quả của bài toán đó. Trong quá trình giải quyết bài toán, có thể sẽ gọi đệ quy để giải quyết các bài toán con, và các kết quả của các bài toán con đó sẽ được sử dụng để tính toán kết quả của bài toán gốc.

## Ví dụ
Input: Tính tổng các số từ 1 đến n, với n được nhập từ bàn phím.

Output: Tổng các số từ 1 đến n.

## Ứng dụng
Ứng dụng: Đệ quy được sử dụng trong nhiều lĩnh vực, bao gồm lập trình máy tính, toán học, khoa học máy tính, v.v. Đệ quy thường được sử dụng để giải quyết các bài toán có cấu trúc đệ quy, như tìm kiếm, sắp xếp, hoặc tính toán trong các cấu trúc dữ liệu như cây hoặc đồ thị.

## Các tính chất bài toán 
- Bài toán đệ quy phải có điểm dừng để tránh việc lặp vô hạn.

- Các bài toán đệ quy thường có thể giải quyết bằng cách chia nhỏ thành các bài toán con.

- Các bài toán đệ quy thường có thể được giải quyết bằng cách sử dụng một hàm đệ quy và một số điều kiện đệ quy.

## Ý tưởng của thuật toán
- Xác định điểm dừng (điều kiện dừng) của bài toán.

- Chia bài toán thành các bài toán con nhỏ hơn và giải chúng bằng cách sử dụng đệ quy.

- Kết hợp các kết quả từ các bài toán con để giải quyết bài toán gốc.

## Mã giả
```c++
int recursiveSum(int n) {
    if (n == 0) {
        return 0;
    }
    return n + recursiveSum(n-1);
}
```

## Cài đặt
```c++
#include <iostream>

using namespace std;

int recursiveSum(int n) {
    if (n == 0) {
        return 0;
    }
    return n + recursiveSum(n-1);
}

int main() {
    int n = 5;
    int sum = recursiveSum(n);
    cout << "Sum of numbers from 1 to " << n << ": " << sum << endl;

    return 0;
}
```

## Đánh giá
_Độ phức tạp của thuật toán:_
- Độ phức tạp thời gian: O(n), vì mỗi lần gọi đệ quy sẽ giảm giá trị của n đến khi n = 0.

- Độ phức tạp không gian: O(n), vì mỗi lần gọi đệ quy sẽ tạo ra một frame mới trên stack.

_Bất biến của thuật toán:_
- Bất biến của thuật toán đệ quy là điểm dừng (điều kiện dừng). Nếu không có điểm dừng, thuật toán sẽ lặp vô hạn.

- Điểm dừng phải được đảm bảo trước khi bắt đầu giải bài toán đệ quy.

## Cải tiến
- Có thể sử dụng kỹ thuật đệ quy đuôi (tail recursion) để giảm độ phức tạp không gian của thuật toán.

- Sử dụng memoization để lưu trữ các kết quả tính toán để tránh tính toán lại các bài toán con trùng lặp.


# Mô phỏng sự kiện

## Input - Output
- Input: Một hệ thống hoặc quá trình được mô tả bằng các sự kiện (event) và các quy tắc hoạt động của hệ thống (system rules).

- Output: Kết quả của quá trình mô phỏng được thực hiện dựa trên các sự kiện và quy tắc của hệ thống.

Trong mô phỏng sự kiện, input là một mô hình của hệ thống bao gồm các sự kiện và quy tắc hoạt động của hệ thống. Các sự kiện đại diện cho các hành động cụ thể mà hệ thống có thể thực hiện, trong khi các quy tắc hoạt động của hệ thống định nghĩa cách các sự kiện tương tác với nhau để tạo ra các kết quả. Output của mô phỏng sự kiện là kết quả của quá trình mô phỏng, được tính toán bằng cách xử lý các sự kiện và các quy tắc của hệ thống.

## Ví dụ
- Input: Mô phỏng một hệ thống hàng đợi, trong đó khách hàng đến và được phục vụ bởi các nhân viên. Khi khách hàng đến, họ được thêm vào hàng đợi. Các nhân viên phục vụ khách hàng theo thứ tự đến trước, và mỗi lần phục vụ mất một khoảng thời gian nhất định. Nếu không có nhân viên trống để phục vụ khách hàng, khách hàng sẽ phải chờ trong hàng đợi.

- Output: Các thống kê về thời gian trung bình mà khách hàng phải chờ đợi và thời gian trung bình mà họ được phục vụ.

## Ứng dụng
Ứng dụng: Mô phỏng sự kiện được sử dụng rộng rãi trong lĩnh vực kỹ thuật và khoa học máy tính để mô phỏng các hệ thống phức tạp, như mạng máy tính, hệ thống điều khiển tự động, hoặc các quá trình sản xuất.

## Các tính chất của bài toán

- Bài toán mô phỏng sự kiện bao gồm các sự kiện và quy tắc hoạt động của hệ thống.

- Các sự kiện được sử dụng để mô tả các hành động cụ thể của hệ thống, trong khi quy tắc hoạt động của hệ thống định nghĩa cách các sự kiện tương tác với nhau.

- Các thống kê được tính toán bằng cách xử lý kết quả của các sự kiện và các quy tắc của hệ thống.


## Ý tưởng thuật toán

- Xác định các sự kiện và quy tắc hoạt động của hệ thống.
Tạo ra một danh sách các sự kiện khởi đầu và sắp xếp chúng theo thứ tự thời gian.
- Thực hiện các sự kiện trong danh sách theo thứ tự và cập nhật trạng thái của hệ thống sau mỗi sự kiện.
Tính toán các thống kê dựa trên kết quả của các sự kiện.

## Mã giả
## Cài đặt
```c++
#include <iostream>
#include <queue>

using namespace std;

class Event {
public:
    double time;
    int type;

    Event(double t, int ty) {
        time = t;
        type = ty;
    }
};

class System {
public:
    double clock;
    int queue_length;
    int servers;
    double service_time;

    System(int s) {
        clock = 0.0;
        queue_length = 0;
        servers = s;
        service_time = 1.0;
    }

    void update_state(Event event) {
        clock = event.time;
        if (event.type == 1) { // Arrival event
            queue_length++;
            if (queue_length <= servers) { // Serve the customer immediately
                double service_completion_time = clock + service_time;
                Event service_completion_event(service_completion_time, 2);
                event_list.push(service_completion_event);
            }
        } else if (event.type == 2) { // Service completion event
            queue_length--;
            if (queue_length >= servers) { // Serve the next customer in queue
                double service_completion_time = clock + service_time;
                Event service_completion_event(service_completion_time, 2);
                event_list.push(service_completion_event);
            }
        }
    }
};

class Statistics {
public:
    double total_waiting_time;
    int customers_served;

    Statistics() {
        total_waiting_time = 0.0;
        customers_served = 0;
    }

    void update_statistics(System system) {
        if (system.queue_length > 0) {
            total_waiting_time += system.queue_length;
            customers_served++;
        }
    }

    double average_waiting_time() {
        return total_waiting_time / customers_served;
    }
};

priority_queue<Event, vector<Event>, function<bool(Event, Event)>> event_list([](Event a, Event b) { return a.time > b.time; });

int main() {
    int num_servers = 2;
    System system(num_servers);
    Statistics statistics();

    // Generate initial events
    double arrival_time = 0.0;
    Event arrival_event(arrival_time, 1);
    event_list.push(arrival_event);

    // Run simulation
    while (!event_list.empty()) {
        Event event = event_list.top();
        event_list.pop();
        system.update_state(event);
        statistics.update_statistics(system);

        // Generate new events
        if (event.type == 1) { // Arrival event
            double next_arrival_time = system.clock + 1.0;
            Event next_arrival_event(next_arrival_time, 1);
            event_list.push(next_arrival_event);
        }
    }

    double avg_waiting_time = statistics.average_waiting_time();
    cout << "Average waiting time: " << avg_waiting_time << endl;

    return 0;
}
```

## Đánh giá

_Độ phức tạp:_

- Độ phức tạp thời gian: Tùy thuộc vào số lượng sự kiện và quy tắc của hệ thống.

- Độ phức tạp không gian: Tùy thuộc vào số lượng sự kiện và quy tắc của hệ thống.

_Bất biến của thuật toán:_

- Các sự kiện được sắp xếp theo thứ tự thời gian.

- Kết quả của mô phỏng sự kiện phụ thuộc vào các sự kiện và quy tắc của hệ thống.

# Luồng cực đại

## Input - Output
_Input:_

- Đồ thị có hướng G = (V, E) với trọng số dương w(u, v) cho mỗi cạnh (u, v) ∈ E

- Đỉnh nguồn s và đỉnh đích t

_Output:_

- Một luồng cực đại từ s đến t trong đồ thị G

## Ví dụ:

Đồ thị G được miêu tả bởi ma trận trọng số sau:


0 16 13 0 0 0<br>
0 0 10 12 0 0<br>
0 4 0 0 14 0<br>
0 0 9 0 0 20<br>
0 0 0 7 0 4<br>
0 0 0 0 0 0<br>


Với đỉnh nguồn s = 0 và đỉnh đích t = 5, ta cần tìm một luồng cực đại từ s đến t trong đồ thị G.


## Ứng dụng:
Tìm kiếm luồng cực đại là một vấn đề quan trọng trong nhiều lĩnh vực như mạng máy tính, sản xuất, vận tải, quản lý tài nguyên nước, v.v.

## Các tính chất của bài toán:

- Một luồng trong đồ thị có hướng là một hàm f: E -> R+ thỏa mãn với mọi (u, v) ∈ E, f(u, v) ≤ w(u, v) (f(u, v) không vượt quá trọng số của cạnh (u, v)).

- Luồng qua một đỉnh u phải bằng tổng các luồng đi vào đỉnh đó trừ đi tổng các luồng đi ra khỏi đỉnh đó.

- Luồng cực đại là luồng có tổng giá trị lớn nhất.

## Ý tưởng thuật toán:
Thuật toán Ford-Fulkerson là một phương pháp cơ bản để tìm luồng cực đại trong đồ thị có hướng. Ý tưởng chính của thuật toán là tìm một đường tăng luồng trong đồ thị và tăng giá trị của luồng trên đường đó. Thuật toán lặp lại cho đến khi không còn đường tăng luồng nào có thể tìm được.

## Mã giả:

1. Khởi tạo luồng ban đầu f(u, v) = 0 với mọi (u, v) thuộc E
2. Lặp lại cho đến khi không còn đường tăng luồng nào:
  a. Tìm một đường tăng luồng p trong đồ thị
  b. Tăng giá trị của luồng trên đường đó
3. Trả về luồng cực đại

## Cài đặt:
Cài đặt thuật toán Ford-Fulkerson trong C++ sử dụng BFS để tìm đường tăng luồng:

```c++
#include <iostream>
#include <queue>
#include <cstring>
#define MAX 1000
using namespace std;

int n, s, t; // số đỉnh, đỉnh nguồn và đỉnh đích
int c[MAX][MAX], f[MAX][MAX], trace[MAX];
// ma trận trọng số, ma trận luồng và mảng trace

bool bfs() {
    queue<int> q;
    q.push(s);
    memset(trace, -1, sizeof(trace)); // Khởi tạo trace = -1
    trace[s] = s;
    while (!q.empty()) {
        int u = q.front(); q.pop();
        for (int v = 0; v < n; v++) {
            if (trace[v] == -1 && c[u][v] > f[u][v]) {
                trace[v] = u;
                if (v == t) return true;
                q.push(v);
            }
        }
    }
    return false;
}

int main() {
    // Nhập đồ thị G
    cin >> n >> s >> t;
    for (int u = 0; u < n; u++) {
        for (int v = 0; v < n; v++) {
            cin >> c[u][v];
        }
    }

    // Tìm luồng cực đại
    int max_flow = 0;
    while (bfs()) {
        int delta = INT_MAX;
        for (int v = t; v != s; v = trace[v]) {
            int u = trace[v];
            delta = min(delta, c[u][v] - f[u][v]);
        }
        for (int v = t; v != s; v = trace[v]) {
            int u = trace[v];
            f[u][v] += delta;
            f[v][u] -= delta;
        }
        max_flow += delta;
    }

    // Xuất kết quả
    cout << max_flow << endl;
    return 0;
} 
```


## Đánh giá:
_Độ phức tạp:_
- Thuật toán Ford-Fulkerson có độ phức tạp thời gian và bộ nhớ khá cao, tùy thuộc vào cách tìm đường tăng luồng. Trong trường hợp tìm đường tăng luồng bằng DFS, độ phức tạp tốt nhất, xấu nhất và trung bình lần lượt là O(Ef), O(Ef^2) và O(E^2flogV), trong đó E là số cạnh trong đồ thị, f là giá trị luồng cực đại và V là số đỉnh trong đồ thị. Tuy nhiên, trong trường hợp cạnh có trọng số âm hoặc không phải là số thực, thuật toán có thể không dẫn đến kết quả chính xác.

_Bất biến của thuật toán:_
- Thuật toán Ford-Fulkerson đảm bảo bất biến của luồng qua một đỉnh và bất biến của giá trị luồng tại mỗi lần lặp. Để giữ bất biến này, ta cần đảm bảo rằng giá trị luồng trên mỗi cạnh không vượt quá trọng số của cạnh đó.

## Cải tiến:
Có nhiều phương pháp cải tiến thuật toán Ford-Fulkerson, ví dụ như thuật toán Edmonds-Karp sử dụng BFS để tìm đường tăng luồng có độ dài ngắn nhất. Thuật toán có độ phức tạp thời gian tốt nhất, xấu nhất và trung bình đều là O(VE^2), trong đó V là số đỉnh và E là số cạnh trong đồ thị. Ngoài ra, thuật toán Dinic sử dụng BFS để tìm các đường tăng luồng có độ dài lớn hơn 1 và có độ phức tạp thời gian tốt nhất, xấu nhất và trung bình đều là O(V^2E).














