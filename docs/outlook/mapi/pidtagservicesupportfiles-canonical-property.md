---
title: PidTagServiceSupportFiles (kanonische Eigenschaft)
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
ms.openlocfilehash: 2dc431d807bd74640e5b5a9c020f668b13530197
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795191"
---
# <a name="pidtagservicesupportfiles-canonical-property"></a><span data-ttu-id="5e0f6-103">PidTagServiceSupportFiles (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="5e0f6-103">PidTagServiceSupportFiles Canonical Property</span></span>

  
  
<span data-ttu-id="5e0f6-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5e0f6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5e0f6-105">Enthält eine Liste der Dateien, die den Dienst angehören.</span><span class="sxs-lookup"><span data-stu-id="5e0f6-105">Contains a list of the files that belong to the message service.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5e0f6-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="5e0f6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5e0f6-107">PR_SERVICE_SUPPORT_FILES, PR_SERVICE_SUPPORT_FILES_A, PR_SERVICE_SUPPORT_FILES_W</span><span class="sxs-lookup"><span data-stu-id="5e0f6-107">PR_SERVICE_SUPPORT_FILES, PR_SERVICE_SUPPORT_FILES_A, PR_SERVICE_SUPPORT_FILES_W</span></span>  <br/> |
|<span data-ttu-id="5e0f6-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="5e0f6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5e0f6-109">0x3D0F</span><span class="sxs-lookup"><span data-stu-id="5e0f6-109">0x3D0F</span></span>  <br/> |
|<span data-ttu-id="5e0f6-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="5e0f6-110">Data type:</span></span>  <br/> |<span data-ttu-id="5e0f6-111">PT_MV_STRING8 PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5e0f6-111">PT_MV_STRING8, PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="5e0f6-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="5e0f6-112">Area:</span></span>  <br/> |<span data-ttu-id="5e0f6-113">MAPI-Profil</span><span class="sxs-lookup"><span data-stu-id="5e0f6-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5e0f6-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5e0f6-114">Remarks</span></span>

<span data-ttu-id="5e0f6-115">Mithilfe eines Dialogfelds in der Systemsteuerungsoption, kann ein Benutzer die Liste der Dateien erhalten, die den Dienst angehören.</span><span class="sxs-lookup"><span data-stu-id="5e0f6-115">Using a dialog box in the control panel applet, a user can obtain the list of files that belong to the message service.</span></span> <span data-ttu-id="5e0f6-116">Beispielsweise kann der Benutzer die Namen der alle Dynamic Link Libraries (DLLs) abgerufen, die mit dem Dienst gehören.</span><span class="sxs-lookup"><span data-stu-id="5e0f6-116">For example, the user can obtain the names of all dynamic-link libraries (DLLs) that belong to the service.</span></span> <span data-ttu-id="5e0f6-117">Der Benutzer kann dann zusätzliche Informationen zu der angegebenen Dateien, beispielsweise den Namen und die Versionsnummern aller DLLs seek.</span><span class="sxs-lookup"><span data-stu-id="5e0f6-117">The user can then seek additional details about the specified files, such as the names and version numbers of all the DLLs.</span></span> <span data-ttu-id="5e0f6-118">MAPI verwendet diese Eigenschaften zum Erstellen einer Support-Datei-Liste in einem Dialogfeld für die Auswahl des Benutzers messaging.</span><span class="sxs-lookup"><span data-stu-id="5e0f6-118">MAPI uses the these properties to create a support file list in a dialog box for messaging user selection.</span></span>
  
<span data-ttu-id="5e0f6-119">MAPI funktioniert nur mit Dateinamen und andere Zeichenfolgen übergeben wurden, in den Zeichensatz für die Active Directory Service Interfaces (ANSI).</span><span class="sxs-lookup"><span data-stu-id="5e0f6-119">MAPI works only with filenames, and other strings passed to it, in the Active Directory Service Interfaces (ANSI) character set.</span></span> <span data-ttu-id="5e0f6-120">Clientanwendungen, die Dateinamen in einem Zeichensatz OEM (Original Equipment Manufacturer) verwenden, müssen sie in ANSI zu konvertieren vor dem Aufruf von MAPI.</span><span class="sxs-lookup"><span data-stu-id="5e0f6-120">Client applications that use filenames in an original equipment manufacturer (OEM) character set must convert them to ANSI before calling MAPI.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5e0f6-121">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="5e0f6-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="5e0f6-122">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="5e0f6-122">Header files</span></span>

<span data-ttu-id="5e0f6-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5e0f6-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="5e0f6-124">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="5e0f6-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="5e0f6-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5e0f6-125">Mapitags.h</span></span>
  
> <span data-ttu-id="5e0f6-126">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="5e0f6-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5e0f6-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5e0f6-127">See also</span></span>



[<span data-ttu-id="5e0f6-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5e0f6-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5e0f6-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5e0f6-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5e0f6-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="5e0f6-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5e0f6-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="5e0f6-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

