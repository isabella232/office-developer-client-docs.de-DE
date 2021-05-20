---
title: Deklarieren von Formularschnittstellen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79283301-e544-4a4d-96c2-3f81dc5b3731
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 0fa742b7ff6d98e3a0f475accbc440d22eac0919
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437511"
---
# <a name="declaring-form-interfaces"></a>Deklarieren von Formularschnittstellen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Sie können die Deklarationen Ihrer Implementierungen von MAPI-Formularschnittstellen vereinfachen, indem Sie die MAPI_ _interface__METHOD-Makros verwenden. Dabei handelt es sich bei der Schnittstelle um eine Formularschnittstelle, die in der Mapiform.h-Headerdatei definiert ist.  Sie müssen diese Makros nicht verwenden, aber andern falls nicht, sollten Sie besonders darauf achten, dass Ihre Deklarationen den Deklarationen in der Mapiform.h-Headerdatei entsprechen. Beispielsweise können Sie die Formularobjektklasse des Formularservers wie folgt deklarieren: 
  
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

