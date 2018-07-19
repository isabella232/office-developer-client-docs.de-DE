---
title: FixMAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 32676003-ba32-886f-1185-4760cb0e30e3
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3c064301a18a8adbfb6109170ed16cb6981d96c2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791681"
---
# <a name="fixmapi"></a><span data-ttu-id="901e2-103">FixMAPI</span><span class="sxs-lookup"><span data-stu-id="901e2-103">FixMAPI</span></span>

  
  
<span data-ttu-id="901e2-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="901e2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="901e2-105">Erstellt eine Sicherungskopie der aktuellen Kopie von mapi32.dll auf dem Client, Computer und Wiederherstellung mapi32.dll mit der MAPI-Bibliothek Stub mapistub.dll.</span><span class="sxs-lookup"><span data-stu-id="901e2-105">Makes a backup copy of the current copy of mapi32.dll on the client computer, and restores mapi32.dll with the MAPI stub library, mapistub.dll.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="901e2-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="901e2-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="901e2-107">Vom exportiert werden:</span><span class="sxs-lookup"><span data-stu-id="901e2-107">Exported by:</span></span>  <br/> |<span data-ttu-id="901e2-108">MAPISTUB.dll</span><span class="sxs-lookup"><span data-stu-id="901e2-108">mapistub.dll</span></span>  <br/> |
|<span data-ttu-id="901e2-109">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="901e2-109">Called by:</span></span>  <br/> |<span data-ttu-id="901e2-110">Client</span><span class="sxs-lookup"><span data-stu-id="901e2-110">Client</span></span>  <br/> |
|<span data-ttu-id="901e2-111">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="901e2-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="901e2-112">Windows</span><span class="sxs-lookup"><span data-stu-id="901e2-112">Windows</span></span>  <br/> |
   
```cpp
DWORD STDAPICALLTYPE FixMAPI(void); 
```

## <a name="return-values"></a><span data-ttu-id="901e2-113">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="901e2-113">Return values</span></span>

<span data-ttu-id="901e2-114">Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Wert ungleich NULL.</span><span class="sxs-lookup"><span data-stu-id="901e2-114">If the function succeeds, the return value is a non-zero value.</span></span>
  
<span data-ttu-id="901e2-115">Wenn die Funktion fehlschlägt, ist der Rückgabewert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="901e2-115">If the function fails, the return value is zero.</span></span> <span data-ttu-id="901e2-116">Wenn Sie erweiterte Fehlerinformationen erhalten möchten, rufen Sie die Microsoft Windows Software Development Kit (SDK)-Funktion, **[GetLastError](http://msdn.microsoft.com/de-de/library/ms679360.aspx)**.</span><span class="sxs-lookup"><span data-stu-id="901e2-116">To get extended error information, call the Microsoft Windows Software Development Kit (SDK) function, **[GetLastError](http://msdn.microsoft.com/de-de/library/ms679360.aspx)**.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="901e2-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="901e2-117">Remarks</span></span>

 <span data-ttu-id="901e2-118">**Fixmapi.exe** ersetzt nicht die aktuelle Datei mapi32.dll, wenn die Datei als schreibgeschützt gekennzeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="901e2-118">**FixMAPI** does not replace the current mapi32.dll file if the file is marked as read-only.</span></span> 
  
 <span data-ttu-id="901e2-119">**Fixmapi.exe** ersetzt die aktuellen mapi32.dll nicht, wenn Microsoft Exchange Server auf dem Computer installiert ist.</span><span class="sxs-lookup"><span data-stu-id="901e2-119">**FixMAPI** does not replace the current mapi32.dll if Microsoft Exchange Server is installed on the computer.</span></span> 
  
<span data-ttu-id="901e2-120">Wenn auf dem Computer eine Sicherungskopie der aktuellen Kopie von mapi32.dll für **Fixmapi.exe** ernannt werden, weist der Sicherungskopie einen Namen "mapi32.dll" unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="901e2-120">When **FixMAPI** makes a backup copy of the current copy of mapi32.dll on the computer, it assigns the backup copy a name different from "mapi32.dll".</span></span> <span data-ttu-id="901e2-121">Klicken Sie dann weist es nachfolgende Aufrufe für diese Assembly in die Sicherungskopie vorgesehen ist.</span><span class="sxs-lookup"><span data-stu-id="901e2-121">It then directs subsequent calls intended for that assembly to the backup copy.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="901e2-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="901e2-122">See also</span></span>



[<span data-ttu-id="901e2-123">KB 256946: Sie erhalten eine Fehlermeldung zu eine Konflikt angezeigt, beim start von Outlook 2000</span><span class="sxs-lookup"><span data-stu-id="901e2-123">KB 256946: You receive a program conflict error message when you start Outlook 2000</span></span>](http://support.microsoft.com/kb/256946)
  
[<span data-ttu-id="901e2-124">KB 228457: Beschreibung des Fixmapi.exe Tools enthalten, mit InternetExplorer 5</span><span class="sxs-lookup"><span data-stu-id="901e2-124">KB 228457: Description of the Fixmapi.exe Tool Included with Internet Explorer 5</span></span>](http://support.microsoft.com/kb/228457)

