---
title: Eigenschaftenbezeichner und -typen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 39a5c97c-5ac8-47a8-b193-a4b3ba6a02a5
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 7f31162e669af6efaf9e935c7c400d105c1321c2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795314"
---
# <a name="property-identifiers-and-types"></a><span data-ttu-id="f4d87-103">Eigenschaftenbezeichner und -typen</span><span class="sxs-lookup"><span data-stu-id="f4d87-103">Property Identifiers and Types</span></span>

  
  
<span data-ttu-id="f4d87-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f4d87-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f4d87-105">Alle MAPI-Eigenschaften werden durch Eigenschaftentags dargestellt.</span><span class="sxs-lookup"><span data-stu-id="f4d87-105">All MAPI properties are represented by property tags.</span></span> <span data-ttu-id="f4d87-106">Ein Eigenschaftentag ist ein 32-Bit-Ganzzahl ohne Vorzeichen-Wert, der Eigenschaftenbezeichner in der besonders enthält, bestellen 16 Bit und den Typ der Eigenschaft in den niedrigen bestellen 16 Bit.</span><span class="sxs-lookup"><span data-stu-id="f4d87-106">A property tag is a 32-bit unsigned integer value that contains the property's identifier in the high order 16 bits and the property's type in the low order 16 bits.</span></span> <span data-ttu-id="f4d87-107">Eigenschaftentags für alle von MAPI definierten Eigenschaften sind in der Headerdatei mapitags.h enthalten.</span><span class="sxs-lookup"><span data-stu-id="f4d87-107">Property tags for all of the properties defined by MAPI are included in the mapitags.h header file.</span></span>
  
<span data-ttu-id="f4d87-108">Eigenschaftenbezeichner werden verwendet, um anzugeben, was für eine Eigenschaft verwendet wird, und wer dafür verantwortlich ist.</span><span class="sxs-lookup"><span data-stu-id="f4d87-108">Property identifiers are used to indicate what a property is used for and who is responsible for it.</span></span> <span data-ttu-id="f4d87-109">Eigenschaftenbezeichner sind MAPI in Bereiche unterteilt; Gibt an, bei denen ein Bezeichner des Bereichs liegt, seine Verwendung und den Besitz.</span><span class="sxs-lookup"><span data-stu-id="f4d87-109">Property identifiers are divided by MAPI into ranges; where an identifier falls in the range indicates its use and ownership.</span></span> 
  
<span data-ttu-id="f4d87-110">Eigenschaftentypen werden verwendet, um das Format für die Eigenschaft Daten anzugeben.</span><span class="sxs-lookup"><span data-stu-id="f4d87-110">Property types are used to indicate the format of the property's data.</span></span> <span data-ttu-id="f4d87-111">MAPI definiert alle gültigen Typen.</span><span class="sxs-lookup"><span data-stu-id="f4d87-111">MAPI defines all of the valid types.</span></span> <span data-ttu-id="f4d87-112">Clients und Erstellen neuer Eigenschaften Dienstanbieter müssen eine der folgenden Typen verwenden.</span><span class="sxs-lookup"><span data-stu-id="f4d87-112">Clients and service providers creating new properties must use one of these types.</span></span> <span data-ttu-id="f4d87-113">Alle die Eigenschaftentypen sind in der Headerdatei mapidefs.h enthalten.</span><span class="sxs-lookup"><span data-stu-id="f4d87-113">All of the property types are included in the mapidefs.h header file.</span></span>
  

