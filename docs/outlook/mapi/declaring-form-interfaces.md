---
title: Deklarieren von Formular Schnittstellen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79283301-e544-4a4d-96c2-3f81dc5b3731
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 8f4d8842efbba2f1f2b7281e5d4741b89f975b3f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791503"
---
# <a name="declaring-form-interfaces"></a>Deklarieren von Formular Schnittstellen

  
  
**Betrifft**: Outlook 
  
Sie können die Deklarationen für die Implementierung von MAPI-Formulars Schnittstellen vereinfachen, indem Sie die MAPI_ _interface__METHOD Makros, wobei _Schnittstelle_ eine Schnittstelle in der Headerdatei Mapiform.h definiert ist. Sie sind nicht erforderlich, um diese Makros verwenden, aber wenn Sie nicht, ergreifen Sie besonders sorgfältig, die die Deklarationen in der Headerdatei Mapiform.h Ihren Deklarationen entsprechen. Beispielsweise können Sie dem Formular Server Formularklasse-Objekt wie folgt deklarieren: 
  
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



[Schreiben von Formularcode Server](writing-form-server-code.md)

