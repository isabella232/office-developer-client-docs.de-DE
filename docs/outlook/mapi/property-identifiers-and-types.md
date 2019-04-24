---
title: Eigenschaftenbezeichner und-Typen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 39a5c97c-5ac8-47a8-b193-a4b3ba6a02a5
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: caba60b7059d1c1f8f0440aeb55abb88801fbc9a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328539"
---
# <a name="property-identifiers-and-types"></a><span data-ttu-id="508af-103">Eigenschaftenbezeichner und-Typen</span><span class="sxs-lookup"><span data-stu-id="508af-103">Property Identifiers and Types</span></span>

  
  
<span data-ttu-id="508af-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="508af-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="508af-105">Alle MAPI-Eigenschaften werden durch Property-Tags dargestellt.</span><span class="sxs-lookup"><span data-stu-id="508af-105">All MAPI properties are represented by property tags.</span></span> <span data-ttu-id="508af-106">Ein Property-Tag ist ein 32-Bit-Ganzzahl ohne Vorzeichen, der den Bezeichner der Eigenschaft in der hochwertigen 16-Bit-Version und den Typ der Eigenschaft in der niedrigen 16-Bit-Reihenfolge enthält.</span><span class="sxs-lookup"><span data-stu-id="508af-106">A property tag is a 32-bit unsigned integer value that contains the property's identifier in the high order 16 bits and the property's type in the low order 16 bits.</span></span> <span data-ttu-id="508af-107">Eigenschaftstags für alle von MAPI definierten Eigenschaften sind in der Headerdatei mapitags. h enthalten.</span><span class="sxs-lookup"><span data-stu-id="508af-107">Property tags for all of the properties defined by MAPI are included in the mapitags.h header file.</span></span>
  
<span data-ttu-id="508af-108">Eigenschaftsbezeichner werden verwendet, um anzugeben, wofür eine Eigenschaft verwendet wird und wer dafür zuständig ist.</span><span class="sxs-lookup"><span data-stu-id="508af-108">Property identifiers are used to indicate what a property is used for and who is responsible for it.</span></span> <span data-ttu-id="508af-109">Eigenschaftsbezeichner werden durch MAPI in Bereiche unterteilt; wo ein Bezeichner in den Range fällt, gibt seine Verwendung und seinen Besitz an.</span><span class="sxs-lookup"><span data-stu-id="508af-109">Property identifiers are divided by MAPI into ranges; where an identifier falls in the range indicates its use and ownership.</span></span> 
  
<span data-ttu-id="508af-110">Eigenschaftstypen werden verwendet, um das Format der Daten der Eigenschaft anzugeben.</span><span class="sxs-lookup"><span data-stu-id="508af-110">Property types are used to indicate the format of the property's data.</span></span> <span data-ttu-id="508af-111">MAPI definiert alle gültigen Typen.</span><span class="sxs-lookup"><span data-stu-id="508af-111">MAPI defines all of the valid types.</span></span> <span data-ttu-id="508af-112">Clients und Dienstanbieter, die neue Eigenschaften erstellen, müssen einen dieser Typen verwenden.</span><span class="sxs-lookup"><span data-stu-id="508af-112">Clients and service providers creating new properties must use one of these types.</span></span> <span data-ttu-id="508af-113">Alle Eigenschaftentypen sind in der Headerdatei mapidefs. h enthalten.</span><span class="sxs-lookup"><span data-stu-id="508af-113">All of the property types are included in the mapidefs.h header file.</span></span>
  

