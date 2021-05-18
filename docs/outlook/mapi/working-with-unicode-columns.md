---
title: Arbeiten mit Unicodespalten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2cd55464-263f-4f83-b874-524271773934
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 76d1afb750dc81b889ca8e5eb3639145c061bfc2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408383"
---
# <a name="working-with-unicode-columns"></a><span data-ttu-id="cb720-103">Arbeiten mit Unicodespalten</span><span class="sxs-lookup"><span data-stu-id="cb720-103">Working with Unicode Columns</span></span>

  
  
<span data-ttu-id="cb720-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cb720-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cb720-105">Zeichenzeichenfolgen in Tabellen können mit standardmäßigen 8-Bit-Zeichen dargestellt werden, bei denen es sich um Eigenschaftentyp PT_STRING8 oder 16-Bit-Unicode-Zeichen handelt, bei denen es sich um Eigenschaftstyptypen PT_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="cb720-105">Character strings in tables can be represented using standard 8-bit characters, which are property type PT_STRING8, or 16-bit Unicode characters, which are property type PT_UNICODE.</span></span> <span data-ttu-id="cb720-106">Tabellen implementierer können auswählen, ob ihre Tabellen Unicode-Zeichenfolgen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="cb720-106">Table implementers are free to choose whether or not their tables support Unicode strings.</span></span> <span data-ttu-id="cb720-107">Da Unicode sowohl für Clients als auch für Dienstanbieter einen Mehrwert bietet, wird die Unterstützung von Unicode nach Möglichkeit empfohlen.</span><span class="sxs-lookup"><span data-stu-id="cb720-107">Because Unicode adds value for both clients and service providers by extending the feature set, supporting Unicode wherever possible is recommended.</span></span> 
  
<span data-ttu-id="cb720-108">Viele Tabellenmethoden akzeptieren ein Flag, das bestimmt, ob Zeichenfolgeneigenschaftswerte Unicode sein sollen.</span><span class="sxs-lookup"><span data-stu-id="cb720-108">Many table methods accept a flag that dictates whether or not string property values are expected to be Unicode.</span></span> <span data-ttu-id="cb720-109">Bei der Eingabe gibt das Angeben des MAPI_UNICODE-Flag an den Tabellen implementier an, dass alle mit dem Aufruf übergebenen Zeichenfolgeneigenschaftswerte Unicode-Zeichenfolgen sind und Eigenschaftentypen von PT_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="cb720-109">On input, specifying the MAPI_UNICODE flag indicates to the table implementer that all string property values passed in with the call are Unicode strings and have property types of PT_UNICODE.</span></span> <span data-ttu-id="cb720-110">Bei der Ausgabe gibt dieses Flag an, dass alle zurückgegebenen Zeichenfolgeneigenschaftswerte nach Möglichkeit Unicode-Zeichenfolgen sein sollten.</span><span class="sxs-lookup"><span data-stu-id="cb720-110">On output, this flag indicates that all returned string property values should be Unicode strings, if possible.</span></span> <span data-ttu-id="cb720-111">Ob das Flag eine Bedeutung für die Eingabe oder Ausgabe hat, hängt von der Methode ab.</span><span class="sxs-lookup"><span data-stu-id="cb720-111">Whether the flag has a meaning for input or output depends on the method.</span></span> <span data-ttu-id="cb720-112">Table implementers that do not support Unicode and are passed the MAPI_UNICODE flag return the MAPI_E_BAD_CHAR_WIDTH value.</span><span class="sxs-lookup"><span data-stu-id="cb720-112">Table implementers that do not support Unicode and are passed the MAPI_UNICODE flag return the MAPI_E_BAD_CHAR_WIDTH value.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cb720-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cb720-113">See also</span></span>



[<span data-ttu-id="cb720-114">MAPI-Tabellen</span><span class="sxs-lookup"><span data-stu-id="cb720-114">MAPI Tables</span></span>](mapi-tables.md)

