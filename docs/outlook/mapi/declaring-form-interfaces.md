---
title: Deklarieren von Formularoberflächen
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
# <a name="declaring-form-interfaces"></a><span data-ttu-id="a297f-103">Deklarieren von Formularoberflächen</span><span class="sxs-lookup"><span data-stu-id="a297f-103">Declaring Form Interfaces</span></span>

  
  
<span data-ttu-id="a297f-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a297f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a297f-105">Sie können die Deklarationen für die Implementierung von MAPI-Formulars Schnittstellen vereinfachen, indem Sie die MAPI_ _interface__METHOD Makros, wobei _Schnittstelle_ eine Schnittstelle in der Headerdatei Mapiform.h definiert ist.</span><span class="sxs-lookup"><span data-stu-id="a297f-105">You can simplify the declarations of your implementations of MAPI form interfaces by using the MAPI_ _interface__METHOD macros, where  _interface_ is a form interface defined in the Mapiform.h header file.</span></span> <span data-ttu-id="a297f-106">Sie sind nicht erforderlich, um diese Makros verwenden, aber wenn Sie nicht, ergreifen Sie besonders sorgfältig, die die Deklarationen in der Headerdatei Mapiform.h Ihren Deklarationen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="a297f-106">You are not required to use these macros, but if you do not, you should take particular care that your declarations conform to the declarations in the Mapiform.h header file.</span></span> <span data-ttu-id="a297f-107">Beispielsweise können Sie dem Formular Server Formularklasse-Objekt wie folgt deklarieren:</span><span class="sxs-lookup"><span data-stu-id="a297f-107">For example, you could declare your form server's form object class like the following:</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="a297f-108">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a297f-108">See also</span></span>



[<span data-ttu-id="a297f-109">Schreiben von Formularservercode</span><span class="sxs-lookup"><span data-stu-id="a297f-109">Writing Form Server Code</span></span>](writing-form-server-code.md)

