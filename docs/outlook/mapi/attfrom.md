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
ms.openlocfilehash: c7c0d1df32a0ad6359fad20128a6a1e3dd225143
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791348"
---
# <a name="attfrom"></a><span data-ttu-id="fff3c-103">attFrom</span><span class="sxs-lookup"><span data-stu-id="fff3c-103">attFrom</span></span>

<span data-ttu-id="fff3c-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fff3c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fff3c-105">Das Attribut **AttFrom** ist als **TRP** Struktur codiert, die den Anzeigenamen und die e-Mail-Adresse des Absenders, gefolgt vom Anzeigenamen und die Adresse des Absenders, gefolgt von erforderlichen Abstände codiert.</span><span class="sxs-lookup"><span data-stu-id="fff3c-105">The **attFrom** attribute is encoded as a **TRP** structure which encodes the display name and email address of the sender, followed by the display name and address of the sender, followed by any necessary padding.</span></span> <span data-ttu-id="fff3c-106">Das Format für **AttFrom** lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="fff3c-106">The format for **attFrom** is as follows:</span></span> 
  
<span data-ttu-id="fff3c-107">**AttFrom**: _TRP-Struktur_ Absender Anzeigenamen _ Absenderadresse _ Textabstand</span><span class="sxs-lookup"><span data-stu-id="fff3c-107">**attFrom**: _TRP-structure_ sender-display-name  _ sender-address _ padding</span></span> 
    
<span data-ttu-id="fff3c-108">Die Absender-Anzeigename ist eine Null endende Zeichenfolge, die Sie bei Bedarf eine 2-Byte-Grenze erreichen mit einem zusätzlichen Null-Zeichen aufgefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="fff3c-108">The sender-display-name is a null-terminated string that is padded with an additional null character, if necessary, to reach a 2-byte boundary.</span></span> <span data-ttu-id="fff3c-109">Der Abstand am Ende der **AttFrom** Codierung besteht aus beliebig viele Null Zeichen Bedarf eine Grenze **sizeof(TRP)** zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="fff3c-109">The padding at the end of the **attFrom** encoding consists of as many null characters as needed to reach a **sizeof(TRP)** boundary.</span></span> 
  
<span data-ttu-id="fff3c-110">_TRP-Struktur:_ **TrpidOneOff** Cbgrtrp Cch cb</span><span class="sxs-lookup"><span data-stu-id="fff3c-110">_TRP-structure:_ **trpidOneOff** cbgrtrp cch cb</span></span> 
    
<span data-ttu-id="fff3c-111">Für das Element der **TRP** **AttFrom** -Struktur ist immer ein einmaligen Codierung, also die Trpid deaktiviert die **TRP**-Strukturfeld wird immer **TrpidOneOff**.</span><span class="sxs-lookup"><span data-stu-id="fff3c-111">For the **attFrom** item, the **TRP**-structure is always a one-off encoding, so the trpid off the **TRP**-structure field is always **trpidOneOff**.</span></span> <span data-ttu-id="fff3c-112">Die Cbgrtrp, Cch und Cb-Elementen entsprechen die verbleibenden Felder der Struktur **TRP** .</span><span class="sxs-lookup"><span data-stu-id="fff3c-112">The cbgrtrp, cch, and cb items correspond to the remaining fields of the **TRP** structure.</span></span> 
  
<span data-ttu-id="fff3c-113">Das Feld Cbgrtrp wird als Summe der berechnet **(sizeof(TRP) \*2)**, die Länge Null endende Absender-Anzeige-Namen seiner Abstand und die Länge Null endende-die Adresse des Absenders.</span><span class="sxs-lookup"><span data-stu-id="fff3c-113">The cbgrtrp field is calculated as the sum of **(sizeof(TRP) \*2)**, the length of the null-terminated sender-display-name with its padding, and the length of the null-terminated sender-address.</span></span>
  
<span data-ttu-id="fff3c-114">Das Feld Cch wird als die Länge des Null endende-Anzeigenamens mit den Textabstand berechnet.</span><span class="sxs-lookup"><span data-stu-id="fff3c-114">The cch field is calculated as the length of the null-terminated display-name with its padding.</span></span>
  
<span data-ttu-id="fff3c-115">Das Cb-Feld ist als die Länge der Absenderadresse Null endende berechnet.</span><span class="sxs-lookup"><span data-stu-id="fff3c-115">The cb field is calculated as the length of the null-terminated sender-address.</span></span>
  
<span data-ttu-id="fff3c-116">_-Absenderadresse:_ Adresstyp **:** beheben **'\0'**</span><span class="sxs-lookup"><span data-stu-id="fff3c-116">_sender-address:_ address-type **:** address **'\0'**</span></span>
    
<span data-ttu-id="fff3c-117">Die Adresse des Absenders ist eine Zeichenfolge, die aus vier Teilen, den Adresstyp, ein literal Doppelpunkt (:)), die Adresse selbst und Endzeichen Null ist.</span><span class="sxs-lookup"><span data-stu-id="fff3c-117">The sender-address is a string that is composed of four parts, the address-type, a literal colon (:), the address itself, and a terminating null character.</span></span> <span data-ttu-id="fff3c-118">Beispielsweise die Zeichenfolge `fax:1-909-555-1234\0` wäre ein rechtliche Absenderadresse-Wert.</span><span class="sxs-lookup"><span data-stu-id="fff3c-118">For example, the string `fax:1-909-555-1234\0` would be a legal sender-address value.</span></span>
  

