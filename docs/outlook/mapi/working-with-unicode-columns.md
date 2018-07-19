---
title: Arbeiten mit Unicode-Spalten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2cd55464-263f-4f83-b874-524271773934
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9f1fd2d4e4bfdc9ccbbb771fedf1141769c8c8ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795844"
---
# <a name="working-with-unicode-columns"></a><span data-ttu-id="d0dc8-103">Arbeiten mit Unicode-Spalten</span><span class="sxs-lookup"><span data-stu-id="d0dc8-103">Working with Unicode Columns</span></span>

  
  
<span data-ttu-id="d0dc8-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d0dc8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d0dc8-105">Zeichenfolgen in Tabellen können mit 8-Bit-Zeichen, die Eigenschaftentyp PT_STRING8 sind, oder 16-Bit-Unicode-Zeichen werden Eigenschaftstyp PT_UNICODE dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="d0dc8-105">Character strings in tables can be represented using standard 8-bit characters, which are property type PT_STRING8, or 16-bit Unicode characters, which are property type PT_UNICODE.</span></span> <span data-ttu-id="d0dc8-106">Tabelle Implementierer können entscheiden, ob ihre Tabellen Unicode-Zeichenfolgen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="d0dc8-106">Table implementers are free to choose whether or not their tables support Unicode strings.</span></span> <span data-ttu-id="d0dc8-107">Da Unicode Wert für Clients und -Dienstanbieter hinzugefügt werden durch die Featuregruppe erweitern, wird empfohlen, mit Unicode-Unterstützung, wann immer möglich.</span><span class="sxs-lookup"><span data-stu-id="d0dc8-107">Because Unicode adds value for both clients and service providers by extending the feature set, supporting Unicode wherever possible is recommended.</span></span> 
  
<span data-ttu-id="d0dc8-108">Viele Table-Methoden akzeptieren eine Kennung, die bestimmt, ob Zeichenfolgenwerte-Eigenschaft erwartet Unicode werden oder nicht.</span><span class="sxs-lookup"><span data-stu-id="d0dc8-108">Many table methods accept a flag that dictates whether or not string property values are expected to be Unicode.</span></span> <span data-ttu-id="d0dc8-109">Bei der Eingabe gibt an, die Option MAPI_UNICODE angeben der Tabelle Implementierer, dass alle Zeichenfolgenwerte für-Eigenschaft zusammen mit dem Aufruf übergeben Unicode-Zeichenfolgen werden und Eigenschaftentypen von PT_UNICODE haben.</span><span class="sxs-lookup"><span data-stu-id="d0dc8-109">On input, specifying the MAPI_UNICODE flag indicates to the table implementer that all string property values passed in with the call are Unicode strings and have property types of PT_UNICODE.</span></span> <span data-ttu-id="d0dc8-110">Bei der Ausgabe gibt dieses Flag an, dass alle Eigenschaftswerte der zurückgegebenen Zeichenfolge Unicode-Zeichenfolgen, wenn möglich sein soll.</span><span class="sxs-lookup"><span data-stu-id="d0dc8-110">On output, this flag indicates that all returned string property values should be Unicode strings, if possible.</span></span> <span data-ttu-id="d0dc8-111">Gibt an, ob das Flag für die Eingabe oder Ausgabe eine Bedeutung hat, hängt von der Methode ab.</span><span class="sxs-lookup"><span data-stu-id="d0dc8-111">Whether the flag has a meaning for input or output depends on the method.</span></span> <span data-ttu-id="d0dc8-112">Tabelle Implementierer, die Unicode nicht unterstützt und sind die Option MAPI_UNICODE übergeben zurück den MAPI_E_BAD_CHAR_WIDTH-Wert.</span><span class="sxs-lookup"><span data-stu-id="d0dc8-112">Table implementers that do not support Unicode and are passed the MAPI_UNICODE flag return the MAPI_E_BAD_CHAR_WIDTH value.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d0dc8-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d0dc8-113">See also</span></span>



[<span data-ttu-id="d0dc8-114">MAPI-Tabellen</span><span class="sxs-lookup"><span data-stu-id="d0dc8-114">MAPI Tables</span></span>](mapi-tables.md)

