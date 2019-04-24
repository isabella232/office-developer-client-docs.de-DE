---
title: FixMAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 32676003-ba32-886f-1185-4760cb0e30e3
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 2aeca1a65a859ac9502995a463bc4869609bcd15
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334961"
---
# <a name="fixmapi"></a><span data-ttu-id="985d1-103">FixMAPI</span><span class="sxs-lookup"><span data-stu-id="985d1-103">FixMAPI</span></span>

  
  
<span data-ttu-id="985d1-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="985d1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="985d1-105">Erstellt eine Sicherungskopie der aktuellen Kopie von MAPI32. dll auf dem Clientcomputer und stellt Mapi32. dll mit der MAPI-Stub-Bibliothek mapistub. dll wieder her.</span><span class="sxs-lookup"><span data-stu-id="985d1-105">Makes a backup copy of the current copy of mapi32.dll on the client computer, and restores mapi32.dll with the MAPI stub library, mapistub.dll.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="985d1-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="985d1-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="985d1-107">Exportiert von:</span><span class="sxs-lookup"><span data-stu-id="985d1-107">Exported by:</span></span>  <br/> |<span data-ttu-id="985d1-108">mapistub. dll</span><span class="sxs-lookup"><span data-stu-id="985d1-108">mapistub.dll</span></span>  <br/> |
|<span data-ttu-id="985d1-109">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="985d1-109">Called by:</span></span>  <br/> |<span data-ttu-id="985d1-110">Client</span><span class="sxs-lookup"><span data-stu-id="985d1-110">Client</span></span>  <br/> |
|<span data-ttu-id="985d1-111">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="985d1-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="985d1-112">Windows</span><span class="sxs-lookup"><span data-stu-id="985d1-112">Windows</span></span>  <br/> |
   
```cpp
DWORD STDAPICALLTYPE FixMAPI(void); 
```

## <a name="return-values"></a><span data-ttu-id="985d1-113">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="985d1-113">Return values</span></span>

<span data-ttu-id="985d1-114">Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Wert ungleich NULL.</span><span class="sxs-lookup"><span data-stu-id="985d1-114">If the function succeeds, the return value is a non-zero value.</span></span>
  
<span data-ttu-id="985d1-115">Wenn die Funktion fehlschlägt, ist der Rückgabewert NULL.</span><span class="sxs-lookup"><span data-stu-id="985d1-115">If the function fails, the return value is zero.</span></span> <span data-ttu-id="985d1-116">Um erweiterte Fehlerinformationen abzurufen, rufen Sie die Microsoft Windows Software Development Kit (SDK)-Funktion, **[getlasterroraufzurufen](https://msdn.microsoft.com/library/ms679360.aspx)**.</span><span class="sxs-lookup"><span data-stu-id="985d1-116">To get extended error information, call the Microsoft Windows Software Development Kit (SDK) function, **[GetLastError](https://msdn.microsoft.com/library/ms679360.aspx)**.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="985d1-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="985d1-117">Remarks</span></span>

 <span data-ttu-id="985d1-118">**Fixmapi** ersetzt die aktuelle Mapi32. dll-Datei nicht, wenn die Datei schreibgeschützt ist.</span><span class="sxs-lookup"><span data-stu-id="985d1-118">**FixMAPI** does not replace the current mapi32.dll file if the file is marked as read-only.</span></span> 
  
 <span data-ttu-id="985d1-119">**Fixmapi** ersetzt nicht die aktuelle Mapi32. dll, wenn Microsoft Exchange Server auf dem Computer installiert ist.</span><span class="sxs-lookup"><span data-stu-id="985d1-119">**FixMAPI** does not replace the current mapi32.dll if Microsoft Exchange Server is installed on the computer.</span></span> 
  
<span data-ttu-id="985d1-120">Wenn **Fixmapi** eine Sicherungskopie der aktuellen Kopie von MAPI32. dll auf dem Computer erstellt, weist es der Sicherungskopie einen anderen Namen als "Mapi32. dll" zu.</span><span class="sxs-lookup"><span data-stu-id="985d1-120">When **FixMAPI** makes a backup copy of the current copy of mapi32.dll on the computer, it assigns the backup copy a name different from "mapi32.dll".</span></span> <span data-ttu-id="985d1-121">Anschließend werden nachfolgende Aufrufe für diese Assembly an die Sicherungskopie weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="985d1-121">It then directs subsequent calls intended for that assembly to the backup copy.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="985d1-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="985d1-122">See also</span></span>



[<span data-ttu-id="985d1-123">KB 256946: Sie erhalten eine Programmkonflikt-Fehlermeldung beim Starten von Outlook 2000</span><span class="sxs-lookup"><span data-stu-id="985d1-123">KB 256946: You receive a program conflict error message when you start Outlook 2000</span></span>](https://support.microsoft.com/kb/256946)
  
[<span data-ttu-id="985d1-124">KB 228457: Beschreibung des in Internet Explorer 5 enthaltenen Fixmapi. exe-Tools</span><span class="sxs-lookup"><span data-stu-id="985d1-124">KB 228457: Description of the Fixmapi.exe Tool Included with Internet Explorer 5</span></span>](https://support.microsoft.com/kb/228457)

