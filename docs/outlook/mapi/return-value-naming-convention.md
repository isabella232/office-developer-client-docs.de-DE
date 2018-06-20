---
title: Rückgabewert Benennungskonvention
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2c1cdd7b-82f1-46f2-a7ce-e0efe857b7cd
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 990a48c661621a3a704236a850f5d09239a12fca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795406"
---
# <a name="return-value-naming-convention"></a><span data-ttu-id="31229-103">Rückgabewert Benennungskonvention</span><span class="sxs-lookup"><span data-stu-id="31229-103">Return Value Naming Convention</span></span>

  
  
<span data-ttu-id="31229-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="31229-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="31229-105">Die MAPICODE. H-Headerdatei enthält viele der Werte, die ein Client oder Dienstanbieter zurückgeben vom eine Implementierung-Methode oder möglicherweise von einem Aufruf zurückgegebene angezeigt.</span><span class="sxs-lookup"><span data-stu-id="31229-105">The MAPICODE.H header file contains many of the values that a client or service provider might return from an interface method implementation or might see returned from a call.</span></span>
  
<span data-ttu-id="31229-106">Die Codes zur Darstellung von Warnungen und Fehler Bedingungen führen Sie eine unterschiedliche Benennungskonvention, die mit dem Präfix MAPI, einem Unterstrich und entweder ein W oder einer E an, dass der Typ des Codes beginnt.</span><span class="sxs-lookup"><span data-stu-id="31229-106">The codes to represent warning and failure conditions follow a different naming convention that begins with the prefix MAPI, an underscore, and either a W or an E to indicate the type of code.</span></span> <span data-ttu-id="31229-107">Der Rest des Codes ist eine kurze Zeichenfolge, um die Bedingung zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="31229-107">The rest of the code is a short character string to describe the condition.</span></span> <span data-ttu-id="31229-108">Jedes Wort in der Zeichenfolge wird durch einen Unterstrich getrennt.</span><span class="sxs-lookup"><span data-stu-id="31229-108">Each word in the string is separated by an underscore.</span></span> <span data-ttu-id="31229-109">Der Fehlerwert MAPI_E_TOO_COMPLEX gibt beispielsweise an, dass die Implementierung nicht verarbeiten kann den Inhalt in den Anruf angefordert wurde.</span><span class="sxs-lookup"><span data-stu-id="31229-109">For example, the error value MAPI_E_TOO_COMPLEX indicates that the implementation could not handle whatever was being requested in the call.</span></span> <span data-ttu-id="31229-110">Schwellenwert für die Warnung MAPI_W_PARTIAL_COMPLETION gibt an, dass der Aufruf war erfolgreich, aber ein Problem aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="31229-110">The warning value MAPI_W_PARTIAL_COMPLETION indicates that the call succeeded, but that there were problems.</span></span> <span data-ttu-id="31229-111">Nur einen Teil der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="31229-111">Only part of the operation was completed successfully.</span></span>
  

