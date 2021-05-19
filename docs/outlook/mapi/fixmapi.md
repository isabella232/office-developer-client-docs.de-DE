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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334961"
---
# <a name="fixmapi"></a><span data-ttu-id="ed9d4-103">FixMAPI</span><span class="sxs-lookup"><span data-stu-id="ed9d4-103">FixMAPI</span></span>

  
  
<span data-ttu-id="ed9d4-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ed9d4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ed9d4-105">Erstellt eine Sicherungskopie der aktuellen Kopie von mapi32.dll auf dem Clientcomputer und stellt mapi32.dll mit der MAPI-Stubbibliothek mapistub.dll.</span><span class="sxs-lookup"><span data-stu-id="ed9d4-105">Makes a backup copy of the current copy of mapi32.dll on the client computer, and restores mapi32.dll with the MAPI stub library, mapistub.dll.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="ed9d4-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="ed9d4-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ed9d4-107">Exportiert von:</span><span class="sxs-lookup"><span data-stu-id="ed9d4-107">Exported by:</span></span>  <br/> |<span data-ttu-id="ed9d4-108">mapistub.dll</span><span class="sxs-lookup"><span data-stu-id="ed9d4-108">mapistub.dll</span></span>  <br/> |
|<span data-ttu-id="ed9d4-109">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="ed9d4-109">Called by:</span></span>  <br/> |<span data-ttu-id="ed9d4-110">Client</span><span class="sxs-lookup"><span data-stu-id="ed9d4-110">Client</span></span>  <br/> |
|<span data-ttu-id="ed9d4-111">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="ed9d4-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="ed9d4-112">Windows</span><span class="sxs-lookup"><span data-stu-id="ed9d4-112">Windows</span></span>  <br/> |
   
```cpp
DWORD STDAPICALLTYPE FixMAPI(void); 
```

## <a name="return-values"></a><span data-ttu-id="ed9d4-113">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="ed9d4-113">Return values</span></span>

<span data-ttu-id="ed9d4-114">Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Nicht-Null-Wert.</span><span class="sxs-lookup"><span data-stu-id="ed9d4-114">If the function succeeds, the return value is a non-zero value.</span></span>
  
<span data-ttu-id="ed9d4-115">Wenn die Funktion fehlschlägt, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="ed9d4-115">If the function fails, the return value is zero.</span></span> <span data-ttu-id="ed9d4-116">Rufen Sie die Microsoft Windows Software Development Kit (SDK)-Funktion **[GetLastError](https://msdn.microsoft.com/library/ms679360.aspx)** auf, um erweiterte Fehlerinformationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ed9d4-116">To get extended error information, call the Microsoft Windows Software Development Kit (SDK) function, **[GetLastError](https://msdn.microsoft.com/library/ms679360.aspx)**.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ed9d4-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ed9d4-117">Remarks</span></span>

 <span data-ttu-id="ed9d4-118">**FixMAPI** ersetzt nicht die aktuelle mapi32.dll, wenn die Datei als schreibgeschützt gekennzeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="ed9d4-118">**FixMAPI** does not replace the current mapi32.dll file if the file is marked as read-only.</span></span> 
  
 <span data-ttu-id="ed9d4-119">**FixMAPI** ersetzt nicht die aktuelle mapi32.dll, Microsoft Exchange Server auf dem Computer installiert ist.</span><span class="sxs-lookup"><span data-stu-id="ed9d4-119">**FixMAPI** does not replace the current mapi32.dll if Microsoft Exchange Server is installed on the computer.</span></span> 
  
<span data-ttu-id="ed9d4-120">Wenn **FixMAPI** eine Sicherungskopie der aktuellen Kopie von mapi32.dll auf dem Computer erstellt, weist sie der Sicherungskopie einen anderen Namen zu als "mapi32.dll".</span><span class="sxs-lookup"><span data-stu-id="ed9d4-120">When **FixMAPI** makes a backup copy of the current copy of mapi32.dll on the computer, it assigns the backup copy a name different from "mapi32.dll".</span></span> <span data-ttu-id="ed9d4-121">Anschließend werden nachfolgende Aufrufe, die für diese Assembly vorgesehen sind, an die Sicherungskopie weiter.</span><span class="sxs-lookup"><span data-stu-id="ed9d4-121">It then directs subsequent calls intended for that assembly to the backup copy.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ed9d4-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ed9d4-122">See also</span></span>



[<span data-ttu-id="ed9d4-123">KB 256946: Sie erhalten eine Fehlermeldung zum Programmkonflikt, wenn Sie Outlook 2000 starten</span><span class="sxs-lookup"><span data-stu-id="ed9d4-123">KB 256946: You receive a program conflict error message when you start Outlook 2000</span></span>](https://support.microsoft.com/kb/256946)
  
[<span data-ttu-id="ed9d4-124">KB 228457: Beschreibung des Fixmapi.exe, das in Internet Explorer 5 enthalten ist</span><span class="sxs-lookup"><span data-stu-id="ed9d4-124">KB 228457: Description of the Fixmapi.exe Tool Included with Internet Explorer 5</span></span>](https://support.microsoft.com/kb/228457)

