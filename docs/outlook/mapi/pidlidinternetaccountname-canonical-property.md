---
title: PidLidInternetAccountName (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidInternetAccountName
api_type:
- COM
ms.assetid: 29bedadf-903d-419d-804d-dc8bd92b745d
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 6705b121c58e0ff14726f835c779237cb35c32a9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793626"
---
# <a name="pidlidinternetaccountname-canonical-property"></a><span data-ttu-id="40323-103">PidLidInternetAccountName (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="40323-103">PidLidInternetAccountName Canonical Property</span></span>

  
  
<span data-ttu-id="40323-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="40323-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="40323-105">Gibt den Benutzer sichtbar-e-Mail-Kontonamen über dem e-Mail-Nachricht gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="40323-105">Specifies the user-visible email account name through which the email message is sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="40323-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="40323-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="40323-107">dispidInetAcctName</span><span class="sxs-lookup"><span data-stu-id="40323-107">dispidInetAcctName</span></span>  <br/> |
|<span data-ttu-id="40323-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="40323-108">Property set:</span></span>  <br/> |<span data-ttu-id="40323-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="40323-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="40323-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="40323-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="40323-111">0x00008580</span><span class="sxs-lookup"><span data-stu-id="40323-111">0x00008580</span></span>  <br/> |
|<span data-ttu-id="40323-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="40323-112">Data type:</span></span>  <br/> |<span data-ttu-id="40323-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="40323-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="40323-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="40323-114">Area:</span></span>  <br/> |<span data-ttu-id="40323-115">Allgemeine messaging</span><span class="sxs-lookup"><span data-stu-id="40323-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="40323-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="40323-116">Remarks</span></span>

<span data-ttu-id="40323-117">Das Format dieser Zeichenfolge lautet Implementierung ab.</span><span class="sxs-lookup"><span data-stu-id="40323-117">The format of this string is implementation dependent.</span></span> <span data-ttu-id="40323-118">Diese Eigenschaft kann zum Ermitteln des Servers, leiten Sie die Mail-vom Client verwendet werden, jedoch ist optional, und der Wert hat keine Bedeutung für den Server.</span><span class="sxs-lookup"><span data-stu-id="40323-118">This property can be used by the client to determine which server to direct the mail to, but is optional and the value has no meaning to the server.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="40323-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="40323-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="40323-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="40323-120">Protocol specifications</span></span>

<span data-ttu-id="40323-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="40323-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="40323-122">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="40323-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="40323-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="40323-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="40323-124">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="40323-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="40323-125">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="40323-125">Header files</span></span>

<span data-ttu-id="40323-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="40323-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="40323-127">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="40323-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="40323-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="40323-128">See also</span></span>



[<span data-ttu-id="40323-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="40323-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="40323-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="40323-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="40323-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="40323-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="40323-132">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="40323-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

