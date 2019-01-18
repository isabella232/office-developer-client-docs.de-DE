---
title: Installieren des MAPI-Subsystems
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
api_type:
- COM
ms.assetid: 29fb4c44-1a59-457e-813b-a982bd72891c
description: 'Letzte Änderung: Montag, 9. März 2015'
localization_priority: Priority
ms.openlocfilehash: 112a683f5967f8740c2d21285eb4ebbc0f455c48
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722438"
---
# <a name="installing-the-mapi-subsystem"></a><span data-ttu-id="31336-103">Installieren des MAPI-Subsystems</span><span class="sxs-lookup"><span data-stu-id="31336-103">Installing the MAPI Subsystem</span></span>

  
  
<span data-ttu-id="31336-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="31336-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="31336-105">Unterstützte Versionen von Windows installieren die MAPI-Stub-Bibliothek „Mapi32.dll“ im Ordner _\<Laufwerk\>_ \Windows\System32.</span><span class="sxs-lookup"><span data-stu-id="31336-105">Supported versions of Windows install the MAPI stub library, Mapi32.dll, in the  _\<drive\>_ \Windows\System32 folder.</span></span> 
  
<span data-ttu-id="31336-106">Die folgenden Windows-Versionen werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="31336-106">The supported versions of Windows are as follows:</span></span>
  
- <span data-ttu-id="31336-107">Windows 7.</span><span class="sxs-lookup"><span data-stu-id="31336-107">Windows 7.</span></span>
    
- <span data-ttu-id="31336-108">Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="31336-108">Windows Vista.</span></span>
    
- <span data-ttu-id="31336-109">Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="31336-109">Windows Server 2008.</span></span>
    
- <span data-ttu-id="31336-110">Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="31336-110">Windows Server 2003.</span></span>
    
- <span data-ttu-id="31336-111">Windows XP.</span><span class="sxs-lookup"><span data-stu-id="31336-111">Windows XP.</span></span>
    
<span data-ttu-id="31336-112">Um das MAPI-Subsystem ordnungsgemäß zu installieren, installieren Sie eine Anwendung mit einem MAPI-basierten Speichersubsystem, z. B. Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="31336-112">To correctly install the MAPI subsystem, install an application that contains a MAPI-based subsystem, such as Microsoft Outlook.</span></span>
  
<span data-ttu-id="31336-p101">Informationen zur Installation des MAPI-Subsystems eines Computers finden Sie in der Registrierung. Alle Werte in den Registrierungseinträgen sind Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="31336-p101">You can find information about a computer's MAPI subsystem installation in the system registry. All values in the registry entries are character strings.</span></span> 
  
<span data-ttu-id="31336-115">Installationsprogramme für Nachrichtendienste sind für das Erstellen der Installationsinformationen im folgenden Registrierungsschlüssel verantwortlich:</span><span class="sxs-lookup"><span data-stu-id="31336-115">Message service installation programs are responsible for creating the installation information in the following system registry key:</span></span> 
  
 `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows Messaging Subsystem`
  
<span data-ttu-id="31336-116">Nachrichtendientse müssen der Systemregistrierung Einträge hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="31336-116">Message services must add entries to the system registry.</span></span> 
  
<span data-ttu-id="31336-117">In der folgenden Tabelle ist zusammengefasst, wie Clients Versionsinformationen für das MAPI-Subsystem auf ihrem Computer abrufen.</span><span class="sxs-lookup"><span data-stu-id="31336-117">The following table summarizes how clients retrieve version information for the MAPI subsystem on their computer.</span></span>
  
|<span data-ttu-id="31336-118">**Überprüfen**</span><span class="sxs-lookup"><span data-stu-id="31336-118">**To check**</span></span>|<span data-ttu-id="31336-119">**Registrierung**</span><span class="sxs-lookup"><span data-stu-id="31336-119">**Registry**</span></span>|
|:-----|:-----|
|<span data-ttu-id="31336-120">Verfügbarkeit von MAPI</span><span class="sxs-lookup"><span data-stu-id="31336-120">Availability of MAPI</span></span>  <br/> |<span data-ttu-id="31336-121">Suchen Sie nach  `MAPIX=1`.</span><span class="sxs-lookup"><span data-stu-id="31336-121">Look for  `MAPIX=1`.</span></span>  <br/> |
|<span data-ttu-id="31336-122">Verfügbare Version von MAPI</span><span class="sxs-lookup"><span data-stu-id="31336-122">Available version of MAPI</span></span>  <br/> |<span data-ttu-id="31336-123">Suchen Sie nach einer MAPIXVER-Zeichenfolge in der Form " _x.x.x_".</span><span class="sxs-lookup"><span data-stu-id="31336-123">Look for a MAPIXVER string of the form " _x.x.x_".</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="31336-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="31336-124">See also</span></span>



[<span data-ttu-id="31336-125">Übersicht über die MAPI-Programmierung</span><span class="sxs-lookup"><span data-stu-id="31336-125">MAPI Programming Overview</span></span>](mapi-programming-overview.md)

