# Binary-Search-Flight-Number-Lookup-program-37

def binary_search(arr, target):
    left, right = 0, len(arr)-1
    while left <= right:
        mid = (left + right)//2
        if arr[mid] == target:
            return mid
        elif arr[mid] < target:
            left = mid+1
        else:
            right = mid-1
    return -1

flights = [101,102,103,104,105]  # Sorted
target = 104

index = binary_search(flights, target)
print(f"Flight {target} found at index {index}" if index != -1 else "Flight not found")


Flight 104 found at index 3
