---
title: PidTagProfileHomeServerFQDN (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 80273b50-bc16-4be2-8471-1a127b6786bb
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 398ff2fd4bab49c8279e198e3efa416c53abda7c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794812"
---
# <a name="pidtagprofilehomeserverfqdn-canonical-property"></a><span data-ttu-id="70923-103">PidTagProfileHomeServerFQDN (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="70923-103">PidTagProfileHomeServerFQDN Canonical Property</span></span>

  
  
<span data-ttu-id="70923-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="70923-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="70923-105">Kerberos-Authentifizierung für eine Benutzerprofildienst-Konfiguration aktiviert.</span><span class="sxs-lookup"><span data-stu-id="70923-105">Enables Kerberos authentication of a profile configuration.</span></span>
  
****

|||
|:-----|:-----|
|<span data-ttu-id="70923-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="70923-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="70923-107">PR_PROFILE_HOME_SERVER_FQDN</span><span class="sxs-lookup"><span data-stu-id="70923-107">PR_PROFILE_HOME_SERVER_FQDN</span></span>  <br/> |
|<span data-ttu-id="70923-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="70923-108">Identifier:</span></span>  <br/> |<span data-ttu-id="70923-109">0x662A001F</span><span class="sxs-lookup"><span data-stu-id="70923-109">0x662A001F</span></span>  <br/> |
|<span data-ttu-id="70923-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="70923-110">Data type:</span></span>  <br/> |<span data-ttu-id="70923-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="70923-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="70923-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="70923-112">Area:</span></span>  <br/> |<span data-ttu-id="70923-113">MAPI-Profil-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="70923-113">MAPI profile configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="70923-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="70923-114">Remarks</span></span>

<span data-ttu-id="70923-115">Durch Festlegen dieser Eigenschaft auf den Domänennamen des Verzeichnisservers für die Benutzer kann direkte Verbindung zu den Domänencontroller (DC), die für ein Profil erforderlich ist, die Verwendung von Kerberos-Authentifizierung für Microsoft Exchange Server 2007 konfiguriert wurde und früheren Versionen von **RPC_C_AUTHN_GSS_KERBEROS** in **PR_PROFILE_AUTH_PACKAGE**festlegen.</span><span class="sxs-lookup"><span data-stu-id="70923-115">Setting this property to the Domain Name of the user's directory server allows direct connection to the Domain Controller (DC), which is necessary for a profile that has been configured to use Kerberos authentication against Microsoft Exchange Server 2007 and earlier versions, by setting **RPC_C_AUTHN_GSS_KERBEROS** in **PR_PROFILE_AUTH_PACKAGE**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="70923-116">Microsoft Exchange Server 2010 und Exchange Server 2013 behandeln Adresse Adressbuch Aufrufe an den Client Access Server unterschiedlich gegenüber in der Exchange Server 2007 und früheren Versionen deren Verarbeitung.</span><span class="sxs-lookup"><span data-stu-id="70923-116">Microsoft Exchange Server 2010 and Exchange Server 2013 handle address book calls made to the Client Access Server differently from the way in which Exchange Server 2007 and earlier versions handle them.</span></span> <span data-ttu-id="70923-117">Der DSProxy-Vorgang wird nicht mehr verwendet, damit Kerberos-Authentifizierung erfolgreich ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="70923-117">The DSProxy process is no longer used, so Kerberos authentication may succeed.</span></span> <span data-ttu-id="70923-118">Jedoch der Client noch mit Exchange-Server und nicht direkt mit dem Domänencontroller, die nicht gewünscht werden möglicherweise kommuniziert werden würde: Einstellung **PR_PROFILE_HOME_SERVER_FQDN** vermeidet dies.</span><span class="sxs-lookup"><span data-stu-id="70923-118">However, the client would still be communicating with the Exchange server instead of directly with the DC, which may not be desired: Setting **PR_PROFILE_HOME_SERVER_FQDN** avoids this.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="70923-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="70923-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="70923-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="70923-120">Protocol specifications</span></span>

<span data-ttu-id="70923-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="70923-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="70923-122">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="70923-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="70923-123">[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="70923-123">[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="70923-124">Gibt die zulässige Vorgänge für die Hauptobjekte der Nachricht Store.</span><span class="sxs-lookup"><span data-stu-id="70923-124">Specifies permissible operations for the core message store objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="70923-125">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="70923-125">Header files</span></span>

<span data-ttu-id="70923-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="70923-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="70923-127">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="70923-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="70923-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="70923-128">Mapitags.h</span></span>
  
> <span data-ttu-id="70923-129">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="70923-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="70923-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="70923-130">See also</span></span>



[<span data-ttu-id="70923-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="70923-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="70923-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="70923-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="70923-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="70923-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="70923-134">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="70923-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

