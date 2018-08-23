---
title: PidLidInternetAccountStamp (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidInternetAccountStamp
api_type:
- COM
ms.assetid: 819179fe-e58e-415c-abc7-1949036745ee
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6edbf4e9c1300a7e2e67b1f4226c8e2d05e453c8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585220"
---
# <a name="pidlidinternetaccountstamp-canonical-property"></a><span data-ttu-id="62599-103">PidLidInternetAccountStamp (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="62599-103">PidLidInternetAccountStamp Canonical Property</span></span>

  
  
<span data-ttu-id="62599-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="62599-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="62599-105">Gibt die e-Mail-Konto-ID, die über die die e-Mail-Nachricht gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="62599-105">Specifies the email account ID through which the email message is sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="62599-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="62599-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="62599-107">dispidInetAcctStamp</span><span class="sxs-lookup"><span data-stu-id="62599-107">dispidInetAcctStamp</span></span>  <br/> |
|<span data-ttu-id="62599-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="62599-108">Property set:</span></span>  <br/> |<span data-ttu-id="62599-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="62599-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="62599-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="62599-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="62599-111">0x00008581</span><span class="sxs-lookup"><span data-stu-id="62599-111">0x00008581</span></span>  <br/> |
|<span data-ttu-id="62599-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="62599-112">Data type:</span></span>  <br/> |<span data-ttu-id="62599-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="62599-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="62599-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="62599-114">Area:</span></span>  <br/> |<span data-ttu-id="62599-115">Allgemeine messaging</span><span class="sxs-lookup"><span data-stu-id="62599-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="62599-116">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="62599-116">Remarks</span></span>

<span data-ttu-id="62599-117">Das Format dieser Zeichenfolge lautet Implementierung ab.</span><span class="sxs-lookup"><span data-stu-id="62599-117">The format of this string is implementation dependent.</span></span> <span data-ttu-id="62599-118">Diese Eigenschaft kann zum Ermitteln des Servers, leiten Sie die Mail-vom Client verwendet werden, jedoch ist optional, und der Wert hat keine Bedeutung für den Server.</span><span class="sxs-lookup"><span data-stu-id="62599-118">This property can be used by the client to determine which server to direct the mail to, but is optional and the value has no meaning to the server.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="62599-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="62599-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="62599-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="62599-120">Protocol specifications</span></span>

<span data-ttu-id="62599-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="62599-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="62599-122">Enthält Set Eigenschaftendefinition und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="62599-122">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="62599-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="62599-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="62599-124">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="62599-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="62599-125">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="62599-125">Header files</span></span>

<span data-ttu-id="62599-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="62599-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="62599-127">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="62599-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="62599-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="62599-128">See also</span></span>



[<span data-ttu-id="62599-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="62599-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="62599-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="62599-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="62599-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="62599-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="62599-132">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="62599-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

