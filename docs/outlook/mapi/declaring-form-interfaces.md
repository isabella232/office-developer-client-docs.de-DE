---
title: Deklarieren von Formular Schnittstellen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79283301-e544-4a4d-96c2-3f81dc5b3731
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 0fa742b7ff6d98e3a0f475accbc440d22eac0919
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337058"
---
# <a name="declaring-form-interfaces"></a>Deklarieren von Formular Schnittstellen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Sie können die Deklarationen ihrer Implementierungen von MAPI-Formular Schnittstellen vereinfachen, indem Sie die MAPI_-_interface__METHOD-Makros verwenden, wobei _Interface_ eine in der Headerdatei Mapiform. h definierte Formularschnittstelle ist. Sie müssen diese Makros nicht verwenden, aber wenn Sie dies nicht tun, sollten Sie besonders darauf achten, dass ihre Deklarationen den Deklarationen in der Headerdatei Mapiform. h entsprechen. Sie können beispielsweise die Formularobjekt Klasse Ihres Formular Servers wie folgt deklarieren: 
  
```cpp
class CMyForm : public IPersistMessage, public IMAPIForm,
                public IMAPIFormAdviseSink
{
public:
    CMyForm(CClassFactory *);    // constructorr takes a class factory object
    ~CMyForm(void);
// MAPI methods that need to be implemented.
    MAPI_IUNKNOWN_METHODS(IMPL);
    MAPI_GETLASTERROR_METHOD(IMPL);
    MAPI_IPERSISTMESSAGE_METHODS(IMPL);
    MAPI_IMAPIFORM_METHODS(IMPL);
    MAPI_IMAPIFORMADVISESINK_METHODS(IMPL);
// Add other implementation specific items.
};

```

## <a name="see-also"></a>Siehe auch



[Schreiben von Formular Server Code](writing-form-server-code.md)

