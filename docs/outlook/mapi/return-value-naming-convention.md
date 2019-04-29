---
title: BeNennungsKonvention für Rückgabewerte
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
# <a name="return-value-naming-convention"></a><span data-ttu-id="4ef75-103">BeNennungsKonvention für Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="4ef75-103">Return Value Naming Convention</span></span>

  
  
<span data-ttu-id="4ef75-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4ef75-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4ef75-105">Die MAPICODE. H-Headerdatei enthält viele der Werte, die ein Client oder Dienstanbieter von einer Implementierung der Schnittstellenmethode zurückgeben kann oder von einem Aufruf zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="4ef75-105">The MAPICODE.H header file contains many of the values that a client or service provider might return from an interface method implementation or might see returned from a call.</span></span>
  
<span data-ttu-id="4ef75-106">Die Codes zur Darstellung von Warnungs-und Fehlerbedingungen befolgen eine andere Benennungskonvention, die mit dem Präfix MAPI, einem Unterstrich und einem W-oder E-Wert beginnt, um den Typ des Codes anzugeben.</span><span class="sxs-lookup"><span data-stu-id="4ef75-106">The codes to represent warning and failure conditions follow a different naming convention that begins with the prefix MAPI, an underscore, and either a W or an E to indicate the type of code.</span></span> <span data-ttu-id="4ef75-107">Der Rest des Codes ist eine kurze Zeichenfolge zur Beschreibung der Bedingung.</span><span class="sxs-lookup"><span data-stu-id="4ef75-107">The rest of the code is a short character string to describe the condition.</span></span> <span data-ttu-id="4ef75-108">Jedes Wort in der Zeichenfolge wird durch einen Unterstrich getrennt.</span><span class="sxs-lookup"><span data-stu-id="4ef75-108">Each word in the string is separated by an underscore.</span></span> <span data-ttu-id="4ef75-109">Der Fehlerwert MAPI_E_TOO_COMPLEX gibt beispielsweise an, dass die Implementierung nicht verarbeiten konnte, was im Aufruf angefordert wurde.</span><span class="sxs-lookup"><span data-stu-id="4ef75-109">For example, the error value MAPI_E_TOO_COMPLEX indicates that the implementation could not handle whatever was being requested in the call.</span></span> <span data-ttu-id="4ef75-110">Der Warnungswert MAPI_W_PARTIAL_COMPLETION gibt an, dass der Aufruf erfolgreich war, aber Probleme aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="4ef75-110">The warning value MAPI_W_PARTIAL_COMPLETION indicates that the call succeeded, but that there were problems.</span></span> <span data-ttu-id="4ef75-111">Nur ein Teil des Vorgangs wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="4ef75-111">Only part of the operation was completed successfully.</span></span>
  

