---
title: Kanonische Pidtagprofilehomeserverfqdn (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 80273b50-bc16-4be2-8471-1a127b6786bb
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: aef4a932da35f3c4955bc2f4b265b146775c6d87
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341594"
---
# <a name="pidtagprofilehomeserverfqdn-canonical-property"></a><span data-ttu-id="0f7f3-103">Kanonische Pidtagprofilehomeserverfqdn (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0f7f3-103">PidTagProfileHomeServerFQDN Canonical Property</span></span>

  
  
<span data-ttu-id="0f7f3-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0f7f3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0f7f3-105">Aktiviert die Kerberos-Authentifizierung einer Profilkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="0f7f3-105">Enables Kerberos authentication of a profile configuration.</span></span>
  
****

|||
|:-----|:-----|
|<span data-ttu-id="0f7f3-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="0f7f3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0f7f3-107">PR_PROFILE_HOME_SERVER_FQDN</span><span class="sxs-lookup"><span data-stu-id="0f7f3-107">PR_PROFILE_HOME_SERVER_FQDN</span></span>  <br/> |
|<span data-ttu-id="0f7f3-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="0f7f3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0f7f3-109">0x662A001F</span><span class="sxs-lookup"><span data-stu-id="0f7f3-109">0x662A001F</span></span>  <br/> |
|<span data-ttu-id="0f7f3-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="0f7f3-110">Data type:</span></span>  <br/> |<span data-ttu-id="0f7f3-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0f7f3-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="0f7f3-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="0f7f3-112">Area:</span></span>  <br/> |<span data-ttu-id="0f7f3-113">MAPI-Profilkonfiguration</span><span class="sxs-lookup"><span data-stu-id="0f7f3-113">MAPI profile configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0f7f3-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0f7f3-114">Remarks</span></span>

<span data-ttu-id="0f7f3-115">Wenn Sie diese Eigenschaft auf den Domänennamen des Verzeichnisservers des Benutzers festlegen, ist eine direkte Verbindung mit dem Domänen Controller (DC) möglich, der für ein Profil erforderlich ist, das für die Verwendung der Kerberos-Authentifizierung für Microsoft Exchange Server 2007 konfiguriert wurde und frühere Versionen, durch Festlegen von **RPC_C_AUTHN_GSS_KERBEROS** in **PR_PROFILE_AUTH_PACKAGE**.</span><span class="sxs-lookup"><span data-stu-id="0f7f3-115">Setting this property to the Domain Name of the user's directory server allows direct connection to the Domain Controller (DC), which is necessary for a profile that has been configured to use Kerberos authentication against Microsoft Exchange Server 2007 and earlier versions, by setting **RPC_C_AUTHN_GSS_KERBEROS** in **PR_PROFILE_AUTH_PACKAGE**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="0f7f3-116">Microsoft Exchange Server 2010 und Exchange Server 2013 behandeln Adressbuch Aufrufe, die auf dem Client Zugriffs Server vorgenommen wurden, anders als die Art und Weise, in der Sie von Exchange Server 2007 und früheren Versionen verarbeitet wurden.</span><span class="sxs-lookup"><span data-stu-id="0f7f3-116">Microsoft Exchange Server 2010 and Exchange Server 2013 handle address book calls made to the Client Access Server differently from the way in which Exchange Server 2007 and earlier versions handle them.</span></span> <span data-ttu-id="0f7f3-117">Der DSProxy-Prozess wird nicht mehr verwendet, sodass die Kerberos-Authentifizierung möglicherweise erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0f7f3-117">The DSProxy process is no longer used, so Kerberos authentication may succeed.</span></span> <span data-ttu-id="0f7f3-118">Der Client würde jedoch weiterhin mit dem Exchange-Server und nicht direkt mit dem DC kommunizieren, was möglicherweise nicht erwünscht ist: die Einstellung **PR_PROFILE_HOME_SERVER_FQDN** vermeidet dies.</span><span class="sxs-lookup"><span data-stu-id="0f7f3-118">However, the client would still be communicating with the Exchange server instead of directly with the DC, which may not be desired: Setting **PR_PROFILE_HOME_SERVER_FQDN** avoids this.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="0f7f3-119">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="0f7f3-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0f7f3-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="0f7f3-120">Protocol specifications</span></span>

<span data-ttu-id="0f7f3-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0f7f3-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0f7f3-122">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="0f7f3-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0f7f3-123">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0f7f3-123">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0f7f3-124">Gibt zulässige Vorgänge für die wichtigsten Nachrichtenspeicher Objekte an.</span><span class="sxs-lookup"><span data-stu-id="0f7f3-124">Specifies permissible operations for the core message store objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0f7f3-125">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="0f7f3-125">Header files</span></span>

<span data-ttu-id="0f7f3-126">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="0f7f3-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="0f7f3-127">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="0f7f3-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="0f7f3-128">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="0f7f3-128">Mapitags.h</span></span>
  
> <span data-ttu-id="0f7f3-129">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="0f7f3-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0f7f3-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0f7f3-130">See also</span></span>



[<span data-ttu-id="0f7f3-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0f7f3-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0f7f3-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0f7f3-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0f7f3-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="0f7f3-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0f7f3-134">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="0f7f3-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

