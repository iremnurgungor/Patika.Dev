def flatten(lst):
    flat_list = []
    for item in lst:
        if isinstance(item, list):  # Eğer item bir listeyse
            flat_list.extend(flatten(item))  # recursive olarak içeriğini aç
        else:
            flat_list.append(item)  # değilse direkt ekle
    return flat_list

# Test
input_list = [[1,'a',['cat'],2],[[[3]],'dog'],4,5]
print(flatten(input_list))  
# Çıktı: [1, 'a', 'cat', 2, 3, 'dog', 4, 5]
