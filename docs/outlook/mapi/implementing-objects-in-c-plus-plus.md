---
title: Implementieren von Objekten in C++
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d1a050ff-3cf9-4bf7-812d-b7c1b31056e7
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 4c233f9855674080496b2e54ba9548a53738ead8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574727"
---
# <a name="implementing-objects-in-c"></a><span data-ttu-id="252f1-103">Implementieren von Objekten in C++</span><span class="sxs-lookup"><span data-stu-id="252f1-103">Implementing objects in C++</span></span>

<span data-ttu-id="252f1-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="252f1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="252f1-105">C++-Clients und -Dienstanbieter definieren MAPI-Objekten durch Erstellen von Klassen, die von den Schnittstellen erben, die sie implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="252f1-105">C++ clients and service providers define MAPI objects by creating classes that inherit from the interfaces they are implementing.</span></span> <span data-ttu-id="252f1-106">Jede-Schnittstellenmethoden ist öffentlich, wie der Konstruktor und der Destruktor für die Klasse sind.</span><span class="sxs-lookup"><span data-stu-id="252f1-106">Each of the interface methods is public, as are the constructor and destructor for the class.</span></span> <span data-ttu-id="252f1-107">Wenn die Klasse zusätzliche Methoden verfügt, können sie öffentliche oder private, je nach der Implementierung werden.</span><span class="sxs-lookup"><span data-stu-id="252f1-107">If the class has additional methods, they can be public or private, depending on the implementation.</span></span> <span data-ttu-id="252f1-108">Alle Datenmember sind privat.</span><span class="sxs-lookup"><span data-stu-id="252f1-108">All data members are private.</span></span> 
  
<span data-ttu-id="252f1-109">Das folgende Codebeispiel veranschaulicht, wie ein C++ Status-Objekt definieren.</span><span class="sxs-lookup"><span data-stu-id="252f1-109">The following example code shows how to define a C++ status object.</span></span> <span data-ttu-id="252f1-110">Die `CMyMAPIObject` Klasse erbt von der [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="252f1-110">The  `CMyMAPIObject` class inherits from the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="252f1-111">Viele der in diesem Beispiel verwendete Makros werden in der OLE-Headerdatei Compobj.h definiert.</span><span class="sxs-lookup"><span data-stu-id="252f1-111">Many of the macros used in this example are defined in the OLE header file Compobj.h.</span></span> <span data-ttu-id="252f1-112">Der erste Member der Klasse sind die Methoden für die Basis-Schnittstelle, gefolgt von den Methoden der geerbten Schnittstellen in der Reihenfolge der Vererbung.</span><span class="sxs-lookup"><span data-stu-id="252f1-112">The first members of the class are the methods of the base interface, followed by the methods of the inherited interfaces in order of inheritance.</span></span> <span data-ttu-id="252f1-113">Befolgen die Schnittstellendefinitionen sind zusätzlichen Methoden, den Konstruktor und Destruktor und die Datenelemente.</span><span class="sxs-lookup"><span data-stu-id="252f1-113">Following the interface definitions are any additional methods, the constructor and destructor, and the data members.</span></span> 
  
```cpp
class  CMyMAPIObject : public IMAPIStatus
{
public:
// Methods of IUnknown.
    STDMETHODIMP QueryInterface (REFIID riid, LPVOID * ppvObj);
    STDMETHODIMP_(ULONG) AddRef ();
    STDMETHODIMP_(ULONG) Release ();
    MAPI_IMAPIPROP_METHODS(IMPL);
    MAPI_IMAPISTATUS_METHODS(IMPL);
// Other methods specific to CMyMAPIObject.
    BOOL WINAPI Method1 ();
    void WINAPI Method2 ();
// Constructors and destructors.
public :
    CMyMAPIObject () {};
    ~CMyMAPIObject () {};
// Data members specific to CMyMAPIObject.
private :
    ULONG               m_cRef;
    CAnotherObj *       m_pObj;
};
 
```

<span data-ttu-id="252f1-114">Verwenden Sie eine Instanz der `CMyMAPIObject` -Klasse, C++-Clients oder Dienstanbieter rufen Sie eine seiner Methoden wie folgt:</span><span class="sxs-lookup"><span data-stu-id="252f1-114">To use an instance of the  `CMyMAPIObject` class, C++ clients or service providers make a call to one of its methods as follows:</span></span> 
  
```cpp
lpMyObj->ValidateState(ulUIParam, ulFlags);

```

## <a name="see-also"></a><span data-ttu-id="252f1-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="252f1-115">See also</span></span>

- [<span data-ttu-id="252f1-116">Implementieren von MAPI-Objekten</span><span class="sxs-lookup"><span data-stu-id="252f1-116">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)

