list_nim = [0, 2, 2, 1, 3, 2, 8]

def rata_rata (deret):
    return sum(deret) / len(deret)
print(f'data = {list_nim}')
print(f'nilai mean = {rata_rata(list_nim)}')
def nilai_tengah(deret):
    deret.sort()
    n = len(deret)
    i_tengah = n // 2

    if n % 2 == 1:
        return deret[i_tengah]

        return (deret[i_tengah - 1] + deret[i_tengah]) /2
print(f'data = {list_nim}')
print(f'nilai median = {nilai_tengah(list_nim)}')

def nilai_terbanyak(deret):
    data_muncul = {}

    for bilangan in deret:
        if bilangan in data_muncul:
            data_muncul[bilangan]+=1
        else:
            data_muncul[bilangan] =1
    bilangan_terbesar = deret[0]
    for bilangan in data_muncul.keys():
        jumlah = data_muncul[bilangan]

        if jumlah>data_muncul[bilangan_terbesar]:
            bilangan_terbesar = bilangan

    return bilangan_terbesar

inputan = input('masukkan data nim anda:')#pisahkan dengan koma setiap data nim anda!
data = [] #contoh data nim saya = 0, 2, 2, 1, 3, 2, 8
for bilangan in inputan.split(','):
    data.append(int(bilangan))

print(f'data = {list_nim}')
print(f'nilai modus = {nilai_terbanyak(list_nim)}')
