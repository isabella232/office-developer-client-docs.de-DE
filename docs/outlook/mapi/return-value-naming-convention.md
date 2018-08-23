---
title: Rückgabewert-Benennungskonvention
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2c1cdd7b-82f1-46f2-a7ce-e0efe857b7cd
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 4d7a95e4681370e1aaf4f8b4c4b7ca0814b3aae7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581846"
---
# <a name="return-value-naming-convention"></a><span data-ttu-id="acd5a-103">Rückgabewert-Benennungskonvention</span><span class="sxs-lookup"><span data-stu-id="acd5a-103">Return Value Naming Convention</span></span>

  
  
<span data-ttu-id="acd5a-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="acd5a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="acd5a-105">Die MAPICODE. H-Headerdatei enthält viele der Werte, die ein Client oder Dienstanbieter zurückgeben vom eine Implementierung-Methode oder möglicherweise von einem Aufruf zurückgegebene angezeigt.</span><span class="sxs-lookup"><span data-stu-id="acd5a-105">The MAPICODE.H header file contains many of the values that a client or service provider might return from an interface method implementation or might see returned from a call.</span></span>
  
<span data-ttu-id="acd5a-106">Die Codes zur Darstellung von Warnungen und Fehler Bedingungen führen Sie eine unterschiedliche Benennungskonvention, die mit dem Präfix MAPI, einem Unterstrich und entweder ein W oder einer E an, dass der Typ des Codes beginnt.</span><span class="sxs-lookup"><span data-stu-id="acd5a-106">The codes to represent warning and failure conditions follow a different naming convention that begins with the prefix MAPI, an underscore, and either a W or an E to indicate the type of code.</span></span> <span data-ttu-id="acd5a-107">Der Rest des Codes ist eine kurze Zeichenfolge, um die Bedingung zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="acd5a-107">The rest of the code is a short character string to describe the condition.</span></span> <span data-ttu-id="acd5a-108">Jedes Wort in der Zeichenfolge wird durch einen Unterstrich getrennt.</span><span class="sxs-lookup"><span data-stu-id="acd5a-108">Each word in the string is separated by an underscore.</span></span> <span data-ttu-id="acd5a-109">Der Fehlerwert MAPI_E_TOO_COMPLEX gibt beispielsweise an, dass die Implementierung nicht verarbeiten kann den Inhalt in den Anruf angefordert wurde.</span><span class="sxs-lookup"><span data-stu-id="acd5a-109">For example, the error value MAPI_E_TOO_COMPLEX indicates that the implementation could not handle whatever was being requested in the call.</span></span> <span data-ttu-id="acd5a-110">Schwellenwert für die Warnung MAPI_W_PARTIAL_COMPLETION gibt an, dass der Aufruf war erfolgreich, aber ein Problem aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="acd5a-110">The warning value MAPI_W_PARTIAL_COMPLETION indicates that the call succeeded, but that there were problems.</span></span> <span data-ttu-id="acd5a-111">Nur einen Teil der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="acd5a-111">Only part of the operation was completed successfully.</span></span>
  

