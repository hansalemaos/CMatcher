<p align="center"><a href="https://twitter.com/Aprender_alemao"><img src="https://cdn.jsdelivr.net/gh/dmhendricks/signature-social-icons/icons/round-flat-filled/50px/twitter.png" alt="Twitter" title="Twitter" width="50"/></a><a href="https://www.facebook.com/estudaralemao/"><img src="https://cdn.jsdelivr.net/gh/dmhendricks/signature-social-icons/icons/round-flat-filled/50px/facebook.png" alt="Facebook" title="Facebook" width="50"/></a><a href="https://www.instagram.com/estudaralemao/"><img src="https://cdn.jsdelivr.net/gh/dmhendricks/signature-social-icons/icons/round-flat-filled/50px/instagram.png" alt="Instagram" title="Instagram" width="50"/></a><a href="https://www.youtube.com/c/wwwqueroestudaralemaocombr"><img src="https://cdn.jsdelivr.net/gh/dmhendricks/signature-social-icons/icons/round-flat-filled/50px/youtube.png" alt="YouTube" title="YouTube" width="50"/></a><a href="https://api.whatsapp.com/send?phone=5511989782756&text=I%20want%20to%20know%20..."><img src="https://cdn.jsdelivr.net/gh/dmhendricks/signature-social-icons/icons/round-flat-filled/50px/whatsapp.png" alt="WhatsApp" title="WhatsApp" width="50"/></a><a href="https://www.queroestudaralemao.com.br"><img src="https://cdn.jsdelivr.net/gh/dmhendricks/signature-social-icons/icons/round-flat-filled/50px/website.png" alt="WWW" title="WWW" width="50"/></a><a href="https://br.pinterest.com/chucrutehans/"><img src="https://cdn.jsdelivr.net/gh/dmhendricks/signature-social-icons/icons/round-flat-filled/50px/pinterest.png" alt="Pinterest" title="Pinterest" width="50"/></a><a href="mailto:aulasparticularesdealemaosp@gmail.com?subject=I%20want%20to%20know%20...%20"><img src="https://cdn.jsdelivr.net/gh/dmhendricks/signature-social-icons/icons/round-flat-filled/50px/mail.png" alt="E-Mail" title="E-Mail" width="50"/>
</a>

<p align="center">
<a href=https://github.com/hansalemaos/CMatcher><img src="https://img.shields.io/badge/author-hansalemaos-black"/></a>
<a href=https://www.queroestudaralemao.com.br><img src="https://img.shields.io/badge/from-queroestudaralemao.com.br-darkgreen"/></a>
<a href=#><img src="https://img.shields.io/badge/for-Windows-black"/></a>
<a href=https://codeload.github.com/liangjingkanji/DrakeTyporaTheme/zip/refs/heads/master><img src="https://img.shields.io/badge/Theme-Drake-black"/></a>
<a href=https://github.com/dmhendricks/signature-social-icons><img src="https://img.shields.io/badge/Social-Icons-darkgreen"/></a>
</p><br><!--  -->

# cmatcher

Use the package to determine the best background and foreground color combinations (e.g. for web page design)
<img src="https://raw.githubusercontent.com/hansalemaos/CMatcher/main/screenshot_.png" alt="Screenshot of Test" title="Screenshot of Test"/>
<br>Just download use 

```python
pip install cmatcher
```

## Here is the code I used to print the stuff on the screenshot

### This is basically everything you need to know

```python
from cmatcher import CMatcher
cormatcher = CMatcher() #create an instance, first time takes longer because a color dataframe will be created and saved to HDD
for x in range(100):
    luminancedifference_from_best_result = choice(range(80,99)) #the higher the number, the less results (more contrast), max is 99
    hsv_difference_from_best_result = choice(range(80,99)) #the higher the number, the less results (more contrast), max is 99
    print(f'{x}. Test - Lum: {luminancedifference_from_best_result} - hsv: {hsv_difference_from_best_result}')
    cormatcher.get_best_contrast_colors(
        color=(choice(range(256)), choice(range(256)), choice(range(256))),
        lum_dif=luminancedifference_from_best_result,
        hsv_dif=hsv_difference_from_best_result,
    ) #this is the most important method, it finds all good combinations
    cormatcher.print_results() #a method to see all results in color
    print(cormatcher.results) #the results are saved in this list
    print('----------------------------------------------------------------------------')
```
