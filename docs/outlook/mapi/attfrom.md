---
title: attFrom
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2d405268-bb33-4863-be38-2d17e8fc956e
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 496bd5439b9f004d3b13d2d73b31b5cac3f9eec9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432415"
---
# <a name="attfrom"></a><span data-ttu-id="51792-103">attFrom</span><span class="sxs-lookup"><span data-stu-id="51792-103">attFrom</span></span>

<span data-ttu-id="51792-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="51792-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="51792-105">Das **attFrom-Attribut** wird als **TRP-Struktur** codiert, die den Anzeigenamen und die E-Mail-Adresse des Absenders codiert, gefolgt vom Anzeigenamen und der Adresse des Absenders, gefolgt von einem erforderlichen Abstand.</span><span class="sxs-lookup"><span data-stu-id="51792-105">The **attFrom** attribute is encoded as a **TRP** structure which encodes the display name and email address of the sender, followed by the display name and address of the sender, followed by any necessary padding.</span></span> <span data-ttu-id="51792-106">Das Format für **attFrom** lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="51792-106">The format for **attFrom** is as follows:</span></span> 
  
<span data-ttu-id="51792-107">**attFrom**: _TRP-structure_ sender-display-name _ sender-address _ padding</span><span class="sxs-lookup"><span data-stu-id="51792-107">**attFrom**: _TRP-structure_ sender-display-name  _ sender-address _ padding</span></span> 
    
<span data-ttu-id="51792-108">Der Sender-display-name ist eine null-beendete Zeichenfolge, die bei Bedarf mit einem zusätzlichen Nullzeichen gepolstert wird, um eine 2-Byte-Grenze zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="51792-108">The sender-display-name is a null-terminated string that is padded with an additional null character, if necessary, to reach a 2-byte boundary.</span></span> <span data-ttu-id="51792-109">Der Abstand am Ende der **attFrom-Codierung** besteht aus so vielen Nullzeichen wie nötig, um eine **Sizeof(TRP)-Grenze zu** erreichen.</span><span class="sxs-lookup"><span data-stu-id="51792-109">The padding at the end of the **attFrom** encoding consists of as many null characters as needed to reach a **sizeof(TRP)** boundary.</span></span> 
  
<span data-ttu-id="51792-110">_TRP-struktur:_ **trpidOneOff** cbgrtrp cch cb</span><span class="sxs-lookup"><span data-stu-id="51792-110">_TRP-structure:_ **trpidOneOff** cbgrtrp cch cb</span></span> 
    
<span data-ttu-id="51792-111">Für das **attFrom-Element** ist die **TRP-Struktur** immer eine einmalige Codierung, daher ist der Trpid aus dem **TRP**-structure-Feld **immer trpidOneOff**.</span><span class="sxs-lookup"><span data-stu-id="51792-111">For the **attFrom** item, the **TRP**-structure is always a one-off encoding, so the trpid off the **TRP**-structure field is always **trpidOneOff**.</span></span> <span data-ttu-id="51792-112">Die cbgrtrp-, cch- und cb-Elemente entsprechen den verbleibenden Feldern der **TRP-Struktur.**</span><span class="sxs-lookup"><span data-stu-id="51792-112">The cbgrtrp, cch, and cb items correspond to the remaining fields of the **TRP** structure.</span></span> 
  
<span data-ttu-id="51792-113">Das cbgrtrp-Feld wird als Summe **von (sizeof(TRP) \* 2),** der Länge des null-terminated sender-display-name mit dem Abstand und der Länge der null-terminated sender-address berechnet.</span><span class="sxs-lookup"><span data-stu-id="51792-113">The cbgrtrp field is calculated as the sum of **(sizeof(TRP) \*2)**, the length of the null-terminated sender-display-name with its padding, and the length of the null-terminated sender-address.</span></span>
  
<span data-ttu-id="51792-114">Das #A0 wird als Länge des mit Null beendeten Anzeigenamens mit seinem Abstand berechnet.</span><span class="sxs-lookup"><span data-stu-id="51792-114">The cch field is calculated as the length of the null-terminated display-name with its padding.</span></span>
  
<span data-ttu-id="51792-115">Das cb-Feld wird als Länge der mit Null beendeten Absenderadresse berechnet.</span><span class="sxs-lookup"><span data-stu-id="51792-115">The cb field is calculated as the length of the null-terminated sender-address.</span></span>
  
<span data-ttu-id="51792-116">_sender-address:_ address-type **:** address **'\0'**</span><span class="sxs-lookup"><span data-stu-id="51792-116">_sender-address:_ address-type **:** address **'\0'**</span></span>
    
<span data-ttu-id="51792-117">Die Absenderadresse ist eine Zeichenfolge, die aus vier Teilen besteht, dem Adresstyp, einem literalen Doppelpunkt (:), der Adresse selbst und einem endenden Nullzeichen.</span><span class="sxs-lookup"><span data-stu-id="51792-117">The sender-address is a string that is composed of four parts, the address-type, a literal colon (:), the address itself, and a terminating null character.</span></span> <span data-ttu-id="51792-118">Die Zeichenfolge wäre z. `fax:1-909-555-1234\0` B. ein gesetzlicher Absenderadressenwert.</span><span class="sxs-lookup"><span data-stu-id="51792-118">For example, the string `fax:1-909-555-1234\0` would be a legal sender-address value.</span></span>
  

