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
ms.openlocfilehash: 2aeca1a65a859ac9502995a463bc4869609bcd15
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383814"
---
# <a name="fixmapi"></a><span data-ttu-id="90537-103">FixMAPI</span><span class="sxs-lookup"><span data-stu-id="90537-103">FixMAPI</span></span>

  
  
<span data-ttu-id="90537-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="90537-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="90537-105">Erstellt eine Sicherungskopie der aktuellen Kopie von mapi32.dll auf dem Client, Computer und Wiederherstellung mapi32.dll mit der MAPI-Bibliothek Stub mapistub.dll.</span><span class="sxs-lookup"><span data-stu-id="90537-105">Makes a backup copy of the current copy of mapi32.dll on the client computer, and restores mapi32.dll with the MAPI stub library, mapistub.dll.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="90537-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="90537-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="90537-107">Vom exportiert werden:</span><span class="sxs-lookup"><span data-stu-id="90537-107">Exported by:</span></span>  <br/> |<span data-ttu-id="90537-108">MAPISTUB.dll</span><span class="sxs-lookup"><span data-stu-id="90537-108">mapistub.dll</span></span>  <br/> |
|<span data-ttu-id="90537-109">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="90537-109">Called by:</span></span>  <br/> |<span data-ttu-id="90537-110">Client</span><span class="sxs-lookup"><span data-stu-id="90537-110">Client</span></span>  <br/> |
|<span data-ttu-id="90537-111">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="90537-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="90537-112">Windows</span><span class="sxs-lookup"><span data-stu-id="90537-112">Windows</span></span>  <br/> |
   
```cpp
DWORD STDAPICALLTYPE FixMAPI(void); 
```

## <a name="return-values"></a><span data-ttu-id="90537-113">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="90537-113">Return values</span></span>

<span data-ttu-id="90537-114">Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Wert ungleich NULL.</span><span class="sxs-lookup"><span data-stu-id="90537-114">If the function succeeds, the return value is a non-zero value.</span></span>
  
<span data-ttu-id="90537-115">Wenn die Funktion fehlschlägt, ist der Rückgabewert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="90537-115">If the function fails, the return value is zero.</span></span> <span data-ttu-id="90537-116">Wenn Sie erweiterte Fehlerinformationen erhalten möchten, rufen Sie die Microsoft Windows Software Development Kit (SDK)-Funktion, **[GetLastError](https://msdn.microsoft.com/library/ms679360.aspx)**.</span><span class="sxs-lookup"><span data-stu-id="90537-116">To get extended error information, call the Microsoft Windows Software Development Kit (SDK) function, **[GetLastError](https://msdn.microsoft.com/library/ms679360.aspx)**.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="90537-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="90537-117">Remarks</span></span>

 <span data-ttu-id="90537-118">**Fixmapi.exe** ersetzt nicht die aktuelle Datei mapi32.dll, wenn die Datei als schreibgeschützt gekennzeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="90537-118">**FixMAPI** does not replace the current mapi32.dll file if the file is marked as read-only.</span></span> 
  
 <span data-ttu-id="90537-119">**Fixmapi.exe** ersetzt die aktuellen mapi32.dll nicht, wenn Microsoft Exchange Server auf dem Computer installiert ist.</span><span class="sxs-lookup"><span data-stu-id="90537-119">**FixMAPI** does not replace the current mapi32.dll if Microsoft Exchange Server is installed on the computer.</span></span> 
  
<span data-ttu-id="90537-120">Wenn auf dem Computer eine Sicherungskopie der aktuellen Kopie von mapi32.dll für **Fixmapi.exe** ernannt werden, weist der Sicherungskopie einen Namen "mapi32.dll" unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="90537-120">When **FixMAPI** makes a backup copy of the current copy of mapi32.dll on the computer, it assigns the backup copy a name different from "mapi32.dll".</span></span> <span data-ttu-id="90537-121">Klicken Sie dann weist es nachfolgende Aufrufe für diese Assembly in die Sicherungskopie vorgesehen ist.</span><span class="sxs-lookup"><span data-stu-id="90537-121">It then directs subsequent calls intended for that assembly to the backup copy.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="90537-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="90537-122">See also</span></span>



[<span data-ttu-id="90537-123">KB 256946: Sie erhalten eine Fehlermeldung zu eine Konflikt angezeigt, beim start von Outlook 2000</span><span class="sxs-lookup"><span data-stu-id="90537-123">KB 256946: You receive a program conflict error message when you start Outlook 2000</span></span>](https://support.microsoft.com/kb/256946)
  
[<span data-ttu-id="90537-124">KB 228457: Beschreibung des Fixmapi.exe Tools enthalten, mit InternetExplorer 5</span><span class="sxs-lookup"><span data-stu-id="90537-124">KB 228457: Description of the Fixmapi.exe Tool Included with Internet Explorer 5</span></span>](https://support.microsoft.com/kb/228457)

