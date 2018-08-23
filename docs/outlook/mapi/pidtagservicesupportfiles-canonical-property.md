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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5165867e46d3d86d65932e7ae432b446efbd8fff
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589126"
---
# <a name="pidtagservicesupportfiles-canonical-property"></a><span data-ttu-id="74759-103">PidTagServiceSupportFiles (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="74759-103">PidTagServiceSupportFiles Canonical Property</span></span>

  
  
<span data-ttu-id="74759-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="74759-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="74759-105">Enthält eine Liste der Dateien, die den Dienst angehören.</span><span class="sxs-lookup"><span data-stu-id="74759-105">Contains a list of the files that belong to the message service.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="74759-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="74759-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="74759-107">PR_SERVICE_SUPPORT_FILES, PR_SERVICE_SUPPORT_FILES_A, PR_SERVICE_SUPPORT_FILES_W</span><span class="sxs-lookup"><span data-stu-id="74759-107">PR_SERVICE_SUPPORT_FILES, PR_SERVICE_SUPPORT_FILES_A, PR_SERVICE_SUPPORT_FILES_W</span></span>  <br/> |
|<span data-ttu-id="74759-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="74759-108">Identifier:</span></span>  <br/> |<span data-ttu-id="74759-109">0x3D0F</span><span class="sxs-lookup"><span data-stu-id="74759-109">0x3D0F</span></span>  <br/> |
|<span data-ttu-id="74759-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="74759-110">Data type:</span></span>  <br/> |<span data-ttu-id="74759-111">PT_MV_STRING8 PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="74759-111">PT_MV_STRING8, PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="74759-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="74759-112">Area:</span></span>  <br/> |<span data-ttu-id="74759-113">MAPI-Profil</span><span class="sxs-lookup"><span data-stu-id="74759-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="74759-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="74759-114">Remarks</span></span>

<span data-ttu-id="74759-115">Mithilfe eines Dialogfelds in der Systemsteuerungsoption, kann ein Benutzer die Liste der Dateien erhalten, die den Dienst angehören.</span><span class="sxs-lookup"><span data-stu-id="74759-115">Using a dialog box in the control panel applet, a user can obtain the list of files that belong to the message service.</span></span> <span data-ttu-id="74759-116">Beispielsweise kann der Benutzer die Namen der alle Dynamic Link Libraries (DLLs) abgerufen, die mit dem Dienst gehören.</span><span class="sxs-lookup"><span data-stu-id="74759-116">For example, the user can obtain the names of all dynamic-link libraries (DLLs) that belong to the service.</span></span> <span data-ttu-id="74759-117">Der Benutzer kann dann zusätzliche Informationen zu der angegebenen Dateien, beispielsweise den Namen und die Versionsnummern aller DLLs seek.</span><span class="sxs-lookup"><span data-stu-id="74759-117">The user can then seek additional details about the specified files, such as the names and version numbers of all the DLLs.</span></span> <span data-ttu-id="74759-118">MAPI verwendet diese Eigenschaften zum Erstellen einer Support-Datei-Liste in einem Dialogfeld für die Auswahl des Benutzers messaging.</span><span class="sxs-lookup"><span data-stu-id="74759-118">MAPI uses the these properties to create a support file list in a dialog box for messaging user selection.</span></span>
  
<span data-ttu-id="74759-119">MAPI funktioniert nur mit Dateinamen und andere Zeichenfolgen übergeben wurden, in den Zeichensatz für die Active Directory Service Interfaces (ANSI).</span><span class="sxs-lookup"><span data-stu-id="74759-119">MAPI works only with filenames, and other strings passed to it, in the Active Directory Service Interfaces (ANSI) character set.</span></span> <span data-ttu-id="74759-120">Clientanwendungen, die Dateinamen in einem Zeichensatz OEM (Original Equipment Manufacturer) verwenden, müssen sie in ANSI zu konvertieren vor dem Aufruf von MAPI.</span><span class="sxs-lookup"><span data-stu-id="74759-120">Client applications that use filenames in an original equipment manufacturer (OEM) character set must convert them to ANSI before calling MAPI.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="74759-121">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="74759-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="74759-122">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="74759-122">Header files</span></span>

<span data-ttu-id="74759-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="74759-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="74759-124">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="74759-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="74759-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="74759-125">Mapitags.h</span></span>
  
> <span data-ttu-id="74759-126">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="74759-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="74759-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="74759-127">See also</span></span>



[<span data-ttu-id="74759-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="74759-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="74759-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="74759-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="74759-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="74759-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="74759-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="74759-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

