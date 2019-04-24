---
title: Kanonische Pidtagservicesupportfiles (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceSupportFiles
api_type:
- COM
ms.assetid: df4be986-62a8-49d6-8eca-25b55c74f830
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 3753177552d45e32e53ae192a9dfae15b601afcc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359472"
---
# <a name="pidtagservicesupportfiles-canonical-property"></a><span data-ttu-id="68d3d-103">Kanonische Pidtagservicesupportfiles (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="68d3d-103">PidTagServiceSupportFiles Canonical Property</span></span>

  
  
<span data-ttu-id="68d3d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="68d3d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="68d3d-105">Enthält eine Liste der Dateien, die zum Nachrichtendienst gehören.</span><span class="sxs-lookup"><span data-stu-id="68d3d-105">Contains a list of the files that belong to the message service.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="68d3d-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="68d3d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="68d3d-107">PR_SERVICE_SUPPORT_FILES, PR_SERVICE_SUPPORT_FILES_A, PR_SERVICE_SUPPORT_FILES_W</span><span class="sxs-lookup"><span data-stu-id="68d3d-107">PR_SERVICE_SUPPORT_FILES, PR_SERVICE_SUPPORT_FILES_A, PR_SERVICE_SUPPORT_FILES_W</span></span>  <br/> |
|<span data-ttu-id="68d3d-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="68d3d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="68d3d-109">0x3D0F</span><span class="sxs-lookup"><span data-stu-id="68d3d-109">0x3D0F</span></span>  <br/> |
|<span data-ttu-id="68d3d-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="68d3d-110">Data type:</span></span>  <br/> |<span data-ttu-id="68d3d-111">PT_MV_STRING8, PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="68d3d-111">PT_MV_STRING8, PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="68d3d-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="68d3d-112">Area:</span></span>  <br/> |<span data-ttu-id="68d3d-113">MAPI-Profil</span><span class="sxs-lookup"><span data-stu-id="68d3d-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="68d3d-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="68d3d-114">Remarks</span></span>

<span data-ttu-id="68d3d-115">Mithilfe eines Dialogfelds in der Systemsteuerung können Benutzer die Liste der Dateien abrufen, die zum Nachrichtendienst gehören.</span><span class="sxs-lookup"><span data-stu-id="68d3d-115">Using a dialog box in the control panel applet, a user can obtain the list of files that belong to the message service.</span></span> <span data-ttu-id="68d3d-116">Der Benutzer kann beispielsweise die Namen aller DLLs (Dynamic Link Libraries) abrufen, die zum Dienst gehören.</span><span class="sxs-lookup"><span data-stu-id="68d3d-116">For example, the user can obtain the names of all dynamic-link libraries (DLLs) that belong to the service.</span></span> <span data-ttu-id="68d3d-117">Der Benutzer kann dann zusätzliche Details zu den angegebenen Dateien suchen, beispielsweise die Namen und Versionsnummern aller DLLs.</span><span class="sxs-lookup"><span data-stu-id="68d3d-117">The user can then seek additional details about the specified files, such as the names and version numbers of all the DLLs.</span></span> <span data-ttu-id="68d3d-118">MAPI verwendet die folgenden Eigenschaften zum Erstellen einer Support Dateiliste in einem Dialogfeld für die Auswahl von Messaging Benutzern.</span><span class="sxs-lookup"><span data-stu-id="68d3d-118">MAPI uses the these properties to create a support file list in a dialog box for messaging user selection.</span></span>
  
<span data-ttu-id="68d3d-119">MAPI funktioniert nur mit Dateinamen und anderen Zeichenfolgen, die an den Zeichensatz der Active Directory-Dienstschnittstellen (ANSI) übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="68d3d-119">MAPI works only with filenames, and other strings passed to it, in the Active Directory Service Interfaces (ANSI) character set.</span></span> <span data-ttu-id="68d3d-120">Client Anwendungen, die Dateinamen in einem OEM-Zeichensatz (Original Equipment Manufacturer) verwenden, müssen Sie vor dem Aufrufen von MAPI in ANSI konvertieren.</span><span class="sxs-lookup"><span data-stu-id="68d3d-120">Client applications that use filenames in an original equipment manufacturer (OEM) character set must convert them to ANSI before calling MAPI.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="68d3d-121">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="68d3d-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="68d3d-122">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="68d3d-122">Header files</span></span>

<span data-ttu-id="68d3d-123">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="68d3d-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="68d3d-124">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="68d3d-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="68d3d-125">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="68d3d-125">Mapitags.h</span></span>
  
> <span data-ttu-id="68d3d-126">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="68d3d-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="68d3d-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="68d3d-127">See also</span></span>



[<span data-ttu-id="68d3d-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="68d3d-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="68d3d-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="68d3d-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="68d3d-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="68d3d-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="68d3d-131">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="68d3d-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

