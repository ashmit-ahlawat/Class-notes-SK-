**code for removing duplicate elements ** 

printf("Enter 10 elements:\n");
for(i = 0; i < n; i++) {
    scanf("%d", &arr[i]);
}

// Removing duplicate elements
for(i = 0; i < n; i++) {
    for(j = i + 1; j < n; j++) {
        if(arr[i] == arr[j]) {
            // Shift elements to left
            for(k = j; k < n - 1; k++) {
                arr[k] = arr[k + 1];
            }
            n--;    // reduce size
            j--;    // check same index again
        }
    }
}

printf("Array after removing duplicates:\n");
for(i = 0; i < n; i++) {
    printf("%d ", arr[i]);
}

return 0;
