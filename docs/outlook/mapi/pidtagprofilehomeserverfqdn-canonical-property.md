---
title: PidTagProfileHomeServerFQDN (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 80273b50-bc16-4be2-8471-1a127b6786bb
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: aef4a932da35f3c4955bc2f4b265b146775c6d87
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400355"
---
# <a name="pidtagprofilehomeserverfqdn-canonical-property"></a><span data-ttu-id="aa5f2-103">PidTagProfileHomeServerFQDN (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="aa5f2-103">PidTagProfileHomeServerFQDN Canonical Property</span></span>

  
  
<span data-ttu-id="aa5f2-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aa5f2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aa5f2-105">Kerberos-Authentifizierung für eine Benutzerprofildienst-Konfiguration aktiviert.</span><span class="sxs-lookup"><span data-stu-id="aa5f2-105">Enables Kerberos authentication of a profile configuration.</span></span>
  
****

|||
|:-----|:-----|
|<span data-ttu-id="aa5f2-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="aa5f2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="aa5f2-107">PR_PROFILE_HOME_SERVER_FQDN</span><span class="sxs-lookup"><span data-stu-id="aa5f2-107">PR_PROFILE_HOME_SERVER_FQDN</span></span>  <br/> |
|<span data-ttu-id="aa5f2-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="aa5f2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="aa5f2-109">0x662A001F</span><span class="sxs-lookup"><span data-stu-id="aa5f2-109">0x662A001F</span></span>  <br/> |
|<span data-ttu-id="aa5f2-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="aa5f2-110">Data type:</span></span>  <br/> |<span data-ttu-id="aa5f2-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="aa5f2-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="aa5f2-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="aa5f2-112">Area:</span></span>  <br/> |<span data-ttu-id="aa5f2-113">MAPI-Profil-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="aa5f2-113">MAPI profile configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="aa5f2-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="aa5f2-114">Remarks</span></span>

<span data-ttu-id="aa5f2-115">Durch Festlegen dieser Eigenschaft auf den Domänennamen des Verzeichnisservers für die Benutzer kann direkte Verbindung zu den Domänencontroller (DC), die für ein Profil erforderlich ist, die Verwendung von Kerberos-Authentifizierung für Microsoft Exchange Server 2007 konfiguriert wurde und früheren Versionen von **RPC_C_AUTHN_GSS_KERBEROS** in **PR_PROFILE_AUTH_PACKAGE**festlegen.</span><span class="sxs-lookup"><span data-stu-id="aa5f2-115">Setting this property to the Domain Name of the user's directory server allows direct connection to the Domain Controller (DC), which is necessary for a profile that has been configured to use Kerberos authentication against Microsoft Exchange Server 2007 and earlier versions, by setting **RPC_C_AUTHN_GSS_KERBEROS** in **PR_PROFILE_AUTH_PACKAGE**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="aa5f2-116">Microsoft Exchange Server 2010 und Exchange Server 2013 behandeln Adresse Adressbuch Aufrufe an den Client Access Server unterschiedlich gegenüber in der Exchange Server 2007 und früheren Versionen deren Verarbeitung.</span><span class="sxs-lookup"><span data-stu-id="aa5f2-116">Microsoft Exchange Server 2010 and Exchange Server 2013 handle address book calls made to the Client Access Server differently from the way in which Exchange Server 2007 and earlier versions handle them.</span></span> <span data-ttu-id="aa5f2-117">Der DSProxy-Vorgang wird nicht mehr verwendet, damit Kerberos-Authentifizierung erfolgreich ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="aa5f2-117">The DSProxy process is no longer used, so Kerberos authentication may succeed.</span></span> <span data-ttu-id="aa5f2-118">Jedoch der Client noch mit Exchange-Server und nicht direkt mit dem Domänencontroller, die nicht gewünscht werden möglicherweise kommuniziert werden würde: Einstellung **PR_PROFILE_HOME_SERVER_FQDN** vermeidet dies.</span><span class="sxs-lookup"><span data-stu-id="aa5f2-118">However, the client would still be communicating with the Exchange server instead of directly with the DC, which may not be desired: Setting **PR_PROFILE_HOME_SERVER_FQDN** avoids this.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="aa5f2-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="aa5f2-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="aa5f2-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="aa5f2-120">Protocol specifications</span></span>

<span data-ttu-id="aa5f2-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aa5f2-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="aa5f2-122">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="aa5f2-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="aa5f2-123">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aa5f2-123">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="aa5f2-124">Gibt die zulässige Vorgänge für die Hauptobjekte der Nachricht Store.</span><span class="sxs-lookup"><span data-stu-id="aa5f2-124">Specifies permissible operations for the core message store objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="aa5f2-125">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="aa5f2-125">Header files</span></span>

<span data-ttu-id="aa5f2-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="aa5f2-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="aa5f2-127">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="aa5f2-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="aa5f2-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="aa5f2-128">Mapitags.h</span></span>
  
> <span data-ttu-id="aa5f2-129">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="aa5f2-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="aa5f2-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aa5f2-130">See also</span></span>



[<span data-ttu-id="aa5f2-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="aa5f2-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="aa5f2-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="aa5f2-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="aa5f2-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="aa5f2-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="aa5f2-134">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="aa5f2-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

