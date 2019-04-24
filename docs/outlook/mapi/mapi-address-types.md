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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32298012"
---
# <a name="mapi-address-types"></a><span data-ttu-id="51322-103">MAPI-Adresstypen</span><span class="sxs-lookup"><span data-stu-id="51322-103">MAPI Address Types</span></span>

  
  
<span data-ttu-id="51322-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="51322-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="51322-105">Jeder Messagingbenutzer ist einem Adresstyp zugeordnet, einer Zeichenfolge, die das Format der Adresse des Benutzers beschreibt, die in der **PR_ADDRTYPE** ([pidtagaddresstype (](pidtagaddresstype-canonical-property.md))-Eigenschaft gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="51322-105">Every messaging user is associated with an address type, a character string describing the format of the user's address that is stored in the **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) property.</span></span> <span data-ttu-id="51322-106">Adresstypen werden Adressformaten zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="51322-106">Address types map to address formats.</span></span> <span data-ttu-id="51322-107">Das heißt, wenn Sie sich den Adresstyp eines Empfängers ansehen, können Clientanwendungen festlegen, wie eine für den Empfänger geeignete Adresse formatiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="51322-107">That is, by looking at a recipient's address type, client applications can determine how to format an address appropriate for the recipient.</span></span> 
  
<span data-ttu-id="51322-108">Der `SMTP` Adresstyp gibt beispielsweise die standardmäßige Internet Adresse an:</span><span class="sxs-lookup"><span data-stu-id="51322-108">For example, the  `SMTP` address type specifies the standard Internet address:</span></span> 
  
 `username@companyname.com.`
  
<span data-ttu-id="51322-109">Und der `EX` Adresstyp gibt eine Exchange-Server Adresse an.</span><span class="sxs-lookup"><span data-stu-id="51322-109">And, the  `EX` address type specifies an Exchange Server address.</span></span> 
  
<span data-ttu-id="51322-110">Alle Adressbucheinträge müssen einen gültigen Adresstyp aufweisen.</span><span class="sxs-lookup"><span data-stu-id="51322-110">All address book entries must have a valid address type.</span></span> <span data-ttu-id="51322-111">Die Benutzer müssen beim Erstellen eines benutzerdefinierten Empfängertyps, der vom Adressbuchanbieter nicht unterstützt wird, einen Adresstyp angeben.</span><span class="sxs-lookup"><span data-stu-id="51322-111">Clients require their users to specify an address type when creating a type of custom recipient unsupported by the address book provider.</span></span> <span data-ttu-id="51322-112">Für die unterstützten Einträge müssen Adressbuchanbieter gültige Adresstypen angeben.</span><span class="sxs-lookup"><span data-stu-id="51322-112">For the entries that they support, address book providers are required to supply valid address types.</span></span> 
  
<span data-ttu-id="51322-113">MAPI definiert nur einen Adresstyp: MAPIPDL, die für die persönliche Verteilerliste steht.</span><span class="sxs-lookup"><span data-stu-id="51322-113">MAPI defines only one address type: MAPIPDL, which stands for personal distribution list.</span></span>
  
<span data-ttu-id="51322-114">Um eine Liste der Adresstypen abzurufen, die von allen Transportanbietern in der Sitzung unterstützt werden, rufen Clientanwendungen die **IMAPISession:: EnumAdrTypes** -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="51322-114">To get a list of the address types supported by all of the transport providers in the session, client applications call the **IMAPISession::EnumAdrTypes** method.</span></span> <span data-ttu-id="51322-115">Weitere Informationen finden Sie unter [IMAPISession:: EnumAdrTypes](imapisession-enumadrtypes.md).</span><span class="sxs-lookup"><span data-stu-id="51322-115">For more information, see [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md).</span></span>
  

