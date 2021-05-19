---
title: Rückgabewertbenennungskonvention
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2c1cdd7b-82f1-46f2-a7ce-e0efe857b7cd
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6786e1ca901215abd709a11401c3026d62c6ffc8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423615"
---
# <a name="return-value-naming-convention"></a><span data-ttu-id="316db-103">Rückgabewertbenennungskonvention</span><span class="sxs-lookup"><span data-stu-id="316db-103">Return Value Naming Convention</span></span>

  
  
<span data-ttu-id="316db-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="316db-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="316db-105">Der MAPICODE. Die H-Headerdatei enthält viele der Werte, die ein Client oder Dienstanbieter von einer Schnittstellenmethodesimplementierung zurückgeben kann oder von einem Aufruf zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="316db-105">The MAPICODE.H header file contains many of the values that a client or service provider might return from an interface method implementation or might see returned from a call.</span></span>
  
<span data-ttu-id="316db-106">Die Codes, die Warnungs- und Fehlerbedingungen darstellen sollen, folgen einer anderen Benennungskonvention, die mit dem Präfix MAPI, einem Unterstrich und entweder einem W oder einem E beginnt, um den Codetyp anzugeben.</span><span class="sxs-lookup"><span data-stu-id="316db-106">The codes to represent warning and failure conditions follow a different naming convention that begins with the prefix MAPI, an underscore, and either a W or an E to indicate the type of code.</span></span> <span data-ttu-id="316db-107">Der Rest des Codes ist eine kurze Zeichenfolge, um die Bedingung zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="316db-107">The rest of the code is a short character string to describe the condition.</span></span> <span data-ttu-id="316db-108">Jedes Wort in der Zeichenfolge wird durch einen Unterstrich getrennt.</span><span class="sxs-lookup"><span data-stu-id="316db-108">Each word in the string is separated by an underscore.</span></span> <span data-ttu-id="316db-109">Beispielsweise gibt der Fehlerwert MAPI_E_TOO_COMPLEX an, dass die Implementierung nicht verarbeiten konnte, was im Aufruf angefordert wurde.</span><span class="sxs-lookup"><span data-stu-id="316db-109">For example, the error value MAPI_E_TOO_COMPLEX indicates that the implementation could not handle whatever was being requested in the call.</span></span> <span data-ttu-id="316db-110">Der Warnwert MAPI_W_PARTIAL_COMPLETION an, dass der Aufruf erfolgreich war, es aber Probleme gab.</span><span class="sxs-lookup"><span data-stu-id="316db-110">The warning value MAPI_W_PARTIAL_COMPLETION indicates that the call succeeded, but that there were problems.</span></span> <span data-ttu-id="316db-111">Nur ein Teil des Vorgangs wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="316db-111">Only part of the operation was completed successfully.</span></span>
  

