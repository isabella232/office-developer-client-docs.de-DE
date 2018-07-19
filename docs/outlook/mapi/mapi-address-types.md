---
title: MAPI-Adresstypen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eee97982-29be-4dcf-ae11-8a38f0080ea7
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 20eb429b2574f67e8b28ae96eeb96f42840123d0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792935"
---
# <a name="mapi-address-types"></a><span data-ttu-id="0beb0-103">MAPI-Adresstypen</span><span class="sxs-lookup"><span data-stu-id="0beb0-103">MAPI Address Types</span></span>

  
  
<span data-ttu-id="0beb0-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0beb0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0beb0-105">Jeder messaging Benutzer ist einen Adresstyp einer Zeichenfolge beschreibt das Format der Adresse des Benutzers, die in der **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))-Eigenschaft gespeichert ist zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="0beb0-105">Every messaging user is associated with an address type, a character string describing the format of the user's address that is stored in the **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) property.</span></span> <span data-ttu-id="0beb0-106">Ordnen Sie Adresstypen Adressformate.</span><span class="sxs-lookup"><span data-stu-id="0beb0-106">Address types map to address formats.</span></span> <span data-ttu-id="0beb0-107">D. h., können Sie anhand des Empfängers Adresstyp, Clientanwendungen wie eine Adresse für den Empfänger formatiert bestimmen.</span><span class="sxs-lookup"><span data-stu-id="0beb0-107">That is, by looking at a recipient's address type, client applications can determine how to format an address appropriate for the recipient.</span></span> 
  
<span data-ttu-id="0beb0-108">Beispielsweise die `SMTP` Adresstyp gibt die standardmäßige Internet-Adresse:</span><span class="sxs-lookup"><span data-stu-id="0beb0-108">For example, the  `SMTP` address type specifies the standard Internet address:</span></span> 
  
 `username@companyname.com.`
  
<span data-ttu-id="0beb0-109">Und, die `EX` Adresstyp gibt eine Exchange Server-Adresse.</span><span class="sxs-lookup"><span data-stu-id="0beb0-109">And, the  `EX` address type specifies an Exchange Server address.</span></span> 
  
<span data-ttu-id="0beb0-110">Alle Einträge im Adressbuch müssen einen gültige Adresstyp verfügen.</span><span class="sxs-lookup"><span data-stu-id="0beb0-110">All address book entries must have a valid address type.</span></span> <span data-ttu-id="0beb0-111">Clients müssen die Benutzer an einer Adresse Geben Sie beim Erstellen eines Typs des benutzerdefinierten Empfänger, die von der Adressbuchanbieter nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0beb0-111">Clients require their users to specify an address type when creating a type of custom recipient unsupported by the address book provider.</span></span> <span data-ttu-id="0beb0-112">Für die Einträge, die sie unterstützen, sind von adressbuchanbietern implementierte erforderlich, um gültige Adresstypen angeben.</span><span class="sxs-lookup"><span data-stu-id="0beb0-112">For the entries that they support, address book providers are required to supply valid address types.</span></span> 
  
<span data-ttu-id="0beb0-113">MAPI nur einen Adresstyp definiert: MAPIPDL, die für persönliche Verteilerliste steht.</span><span class="sxs-lookup"><span data-stu-id="0beb0-113">MAPI defines only one address type: MAPIPDL, which stands for personal distribution list.</span></span>
  
<span data-ttu-id="0beb0-114">Um eine Liste der in der Sitzung von alle Transportanbieter unterstützten Adresstypen erhalten möchten, rufen Sie Clientanwendungen die **IMAPISession::EnumAdrTypes** -Methode.</span><span class="sxs-lookup"><span data-stu-id="0beb0-114">To get a list of the address types supported by all of the transport providers in the session, client applications call the **IMAPISession::EnumAdrTypes** method.</span></span> <span data-ttu-id="0beb0-115">Weitere Informationen finden Sie unter [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md).</span><span class="sxs-lookup"><span data-stu-id="0beb0-115">For more information, see [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md).</span></span>
  

