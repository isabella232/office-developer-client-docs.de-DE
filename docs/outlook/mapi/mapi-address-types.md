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
ms.openlocfilehash: b0ff4ecff7a6e834f1e017adc11244657896db03
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405436"
---
# <a name="mapi-address-types"></a><span data-ttu-id="d5463-103">MAPI-Adresstypen</span><span class="sxs-lookup"><span data-stu-id="d5463-103">MAPI Address Types</span></span>

  
  
<span data-ttu-id="d5463-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d5463-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d5463-105">Jedem Messagingbenutzer ist ein Adresstyp zugeordnet, eine Zeichenzeichenfolge, die das Format der Adresse des Benutzers beschreibt, das in der **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))-Eigenschaft gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="d5463-105">Every messaging user is associated with an address type, a character string describing the format of the user's address that is stored in the **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) property.</span></span> <span data-ttu-id="d5463-106">Adresstypen werden Adressformaten zuordnung.</span><span class="sxs-lookup"><span data-stu-id="d5463-106">Address types map to address formats.</span></span> <span data-ttu-id="d5463-107">Das heißt, durch Einen Blick auf den Adresstyp eines Empfängers können Clientanwendungen bestimmen, wie eine Adresse formatiert wird, die für den Empfänger geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="d5463-107">That is, by looking at a recipient's address type, client applications can determine how to format an address appropriate for the recipient.</span></span> 
  
<span data-ttu-id="d5463-108">Der Adresstyp gibt  `SMTP` z. B. die Standard-Internetadresse an:</span><span class="sxs-lookup"><span data-stu-id="d5463-108">For example, the  `SMTP` address type specifies the standard Internet address:</span></span> 
  
 `username@companyname.com.`
  
<span data-ttu-id="d5463-109">Und der `EX` Adresstyp gibt eine adresse Exchange Server an.</span><span class="sxs-lookup"><span data-stu-id="d5463-109">And, the  `EX` address type specifies an Exchange Server address.</span></span> 
  
<span data-ttu-id="d5463-110">Alle Adressbucheinträge müssen einen gültigen Adresstyp haben.</span><span class="sxs-lookup"><span data-stu-id="d5463-110">All address book entries must have a valid address type.</span></span> <span data-ttu-id="d5463-111">Clients müssen von ihren Benutzern einen Adresstyp angeben, wenn sie einen benutzerdefinierten Empfängertyp erstellen, der vom Adressbuchanbieter nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="d5463-111">Clients require their users to specify an address type when creating a type of custom recipient unsupported by the address book provider.</span></span> <span data-ttu-id="d5463-112">Für die von ihnen unterstützten Einträge müssen Adressbuchanbieter gültige Adresstypen angeben.</span><span class="sxs-lookup"><span data-stu-id="d5463-112">For the entries that they support, address book providers are required to supply valid address types.</span></span> 
  
<span data-ttu-id="d5463-113">MAPI definiert nur einen Adresstyp: MAPIPDL, der für persönliche Verteilerliste steht.</span><span class="sxs-lookup"><span data-stu-id="d5463-113">MAPI defines only one address type: MAPIPDL, which stands for personal distribution list.</span></span>
  
<span data-ttu-id="d5463-114">Um eine Liste der Adresstypen zu erhalten, die von allen Transportanbietern in der Sitzung unterstützt werden, rufen Clientanwendungen die **IMAPISession::EnumAdrTypes-Methode** auf.</span><span class="sxs-lookup"><span data-stu-id="d5463-114">To get a list of the address types supported by all of the transport providers in the session, client applications call the **IMAPISession::EnumAdrTypes** method.</span></span> <span data-ttu-id="d5463-115">Weitere Informationen finden Sie unter [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md).</span><span class="sxs-lookup"><span data-stu-id="d5463-115">For more information, see [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md).</span></span>
  

