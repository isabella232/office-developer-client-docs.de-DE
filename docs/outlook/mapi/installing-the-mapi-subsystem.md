---
title: Installieren des MAPI-Subsystems
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 29fb4c44-1a59-457e-813b-a982bd72891c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c2e135fc031dd3faf5a4e08c50147dfcf7787b5e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792693"
---
# <a name="installing-the-mapi-subsystem"></a><span data-ttu-id="fb205-103">Installieren des MAPI-Subsystems</span><span class="sxs-lookup"><span data-stu-id="fb205-103">Installing the MAPI Subsystem</span></span>

  
  
<span data-ttu-id="fb205-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fb205-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fb205-105">Unterst�tzte Versionen von Windows installieren die MAPI-Stubbibliothek, Mapi32.dll, im Ordner  _\<Laufwerk\>_ \Windows\System32 folder.</span><span class="sxs-lookup"><span data-stu-id="fb205-105">Supported versions of Windows install the MAPI stub library, Mapi32.dll, in the  _\<drive\>_ \Windows\System32 folder.</span></span> 
  
<span data-ttu-id="fb205-106">Die folgenden Windows-Versionen werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="fb205-106">The supported versions of Windows are as follows:</span></span>
  
- <span data-ttu-id="fb205-107">Windows 7.</span><span class="sxs-lookup"><span data-stu-id="fb205-107">Windows 7.</span></span>
    
- <span data-ttu-id="fb205-108">Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="fb205-108">Windows Vista.</span></span>
    
- <span data-ttu-id="fb205-109">Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="fb205-109">Windows Server 2008.</span></span>
    
- <span data-ttu-id="fb205-110">Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="fb205-110">Windows Server 2003.</span></span>
    
- <span data-ttu-id="fb205-111">Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fb205-111">Windows XP.</span></span>
    
<span data-ttu-id="fb205-112">Um das MAPI-Subsystem ordnungsgem�� zu installieren, installieren Sie eine Anwendung mit einem MAPI-basierten Speichersubsystem, z. B. Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="fb205-112">To correctly install the MAPI subsystem, install an application that contains a MAPI-based subsystem, such as Microsoft Outlook.</span></span>
  
<span data-ttu-id="fb205-p101">Informationen zur Installation des MAPI-Subsystems eines Computers finden Sie in der Registrierung. Alle Werte in den Registrierungseinträgen sind Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="fb205-p101">You can find information about a computer's MAPI subsystem installation in the system registry. All values in the registry entries are character strings.</span></span> 
  
<span data-ttu-id="fb205-115">Installationsprogramme für Nachrichtendienste sind für das Erstellen der Installationsinformationen im folgenden Registrierungsschlüssel verantwortlich:</span><span class="sxs-lookup"><span data-stu-id="fb205-115">Message service installation programs are responsible for creating the installation information in the following system registry key:</span></span> 
  
 `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows Messaging Subsystem`
  
<span data-ttu-id="fb205-116">Nachrichtendientse müssen der Systemregistrierung Einträge hinzuf�gen.</span><span class="sxs-lookup"><span data-stu-id="fb205-116">Message services must add entries to the system registry.</span></span> 
  
<span data-ttu-id="fb205-117">In der folgenden Tabelle ist zusammengefasst, wie Clients Versionsinformationen für das MAPI-Subsystem auf ihrem Computer abrufen.</span><span class="sxs-lookup"><span data-stu-id="fb205-117">The following table summarizes how clients retrieve version information for the MAPI subsystem on their computer.</span></span>
  
|<span data-ttu-id="fb205-118">**überpr�fen**</span><span class="sxs-lookup"><span data-stu-id="fb205-118">**To check**</span></span>|<span data-ttu-id="fb205-119">**Registrierung**</span><span class="sxs-lookup"><span data-stu-id="fb205-119">**Registry**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fb205-120">Verfügbarkeit von MAPI</span><span class="sxs-lookup"><span data-stu-id="fb205-120">Availability of MAPI</span></span>  <br/> |<span data-ttu-id="fb205-121">Suchen Sie nach  `MAPIX=1`.</span><span class="sxs-lookup"><span data-stu-id="fb205-121">Look for  `MAPIX=1`.</span></span>  <br/> |
|<span data-ttu-id="fb205-122">Verfügbare Version von MAPI</span><span class="sxs-lookup"><span data-stu-id="fb205-122">Available version of MAPI</span></span>  <br/> |<span data-ttu-id="fb205-123">Suchen Sie nach einer MAPIXVER-Zeichenfolge in der Form " _x.x.x_".</span><span class="sxs-lookup"><span data-stu-id="fb205-123">Look for a MAPIXVER string of the form " _x.x.x_".</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fb205-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fb205-124">See also</span></span>



[<span data-ttu-id="fb205-125">Übersicht über die MAPI-Programmierung</span><span class="sxs-lookup"><span data-stu-id="fb205-125">MAPI Programming Overview</span></span>](mapi-programming-overview.md)

