---
title: Deklarieren von Formularoberflächen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79283301-e544-4a4d-96c2-3f81dc5b3731
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 4687b07c89d866acbe3b6a8f4cde3262657a06b5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584247"
---
# <a name="declaring-form-interfaces"></a>Deklarieren von Formularoberflächen

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
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



[Schreiben von Formularservercode](writing-form-server-code.md)

