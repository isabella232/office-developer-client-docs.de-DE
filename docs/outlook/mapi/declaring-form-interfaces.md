---
title: Deklarieren von Formularschnittstellen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 79283301-e544-4a4d-96c2-3f81dc5b3731
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 19acb1a9c046878b818a61f014711576938a0cf1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584647"
---
# <a name="declaring-form-interfaces"></a>Deklarieren von Formularschnittstellen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Sie können die Deklarationen Ihrer Implementierungen von MAPI-Formularschnittstellen vereinfachen, indem Sie die MAPI_ _interface__METHOD Makros verwenden, wobei  _die Schnittstelle_ eine in der Mapiform.h-Headerdatei definierte Formularschnittstelle ist. Sie müssen diese Makros nicht verwenden, aber wenn Sie dies nicht tun, sollten Sie besonders darauf achten, dass Ihre Deklarationen den Deklarationen in der Headerdatei Mapiform.h entsprechen. Sie können z. B. die Formularobjektklasse des Formularservers wie folgt deklarieren: 
  
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



[Schreiben von Formularservercode](writing-form-server-code.md)

