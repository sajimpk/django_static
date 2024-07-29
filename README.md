# In Settings.py : 
```django
STATIC_URL = 'static/'
MEDIA_URL = 'media/'
STATICFILES_DIRS = [BASE_DIR / 'static', ]
MEDIA_ROOT = BASE_DIR / 'media'
```

# in Project urls.py:

```django
from django.conf import settings
from django.conf.urls.static import static

if settings.DEBUG:
    urlpatterns += static(settings.STATIC_URL, document_root=settings.STATIC_ROOT)
    urlpatterns += static(settings.MEDIA_URL, document_root=settings.MEDIA_ROOT)
```
