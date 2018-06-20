---
title: Transport-Neutral Encapsulation Format (TNEF)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 98d4fe3c-3908-4cd2-bfdb-ff1874a80b24
description: 'Zuletzt geändert: 12 März 2013'
ms.openlocfilehash: 34b64df25cb2f7f591f7c799dec957a0072840dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795755"
---
# <a name="transport-neutral-encapsulation-format-tnef"></a><span data-ttu-id="3ba8b-103">Transport-Neutral Encapsulation Format (TNEF)</span><span class="sxs-lookup"><span data-stu-id="3ba8b-103">Transport-Neutral Encapsulation Format (TNEF)</span></span>

 
  
<span data-ttu-id="3ba8b-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3ba8b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3ba8b-105">TNEF ist ein Format für die Konvertierung von einem Satz von MAPI-Eigenschaften – eine MAPI-Nachricht – in einen seriellen Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="3ba8b-105">TNEF is a format for converting a set of MAPI properties—a MAPI message—into a serial data stream.</span></span> <span data-ttu-id="3ba8b-106">Die TNEF-Funktionen werden in erster Linie von Anbietern Transport verwendet, die müssen MAPI-Eigenschaften für die Übertragung über einem messaging-System zu codieren, die diese Eigenschaften nicht direkt unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3ba8b-106">The TNEF functions are primarily used by transport providers that need to encode MAPI message properties for transmission through a messaging system that does not support those properties directly.</span></span> <span data-ttu-id="3ba8b-107">Beispielsweise verwendet ein SMTP-basierte Transport TNEF zum Codieren von Eigenschaften wie **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)), die keine direkte Darstellungen in der Struktur einer SMTP-Nachricht besitzen.</span><span class="sxs-lookup"><span data-stu-id="3ba8b-107">For example, an SMTP-based transport uses TNEF to encode properties like **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)), which do not have direct representations in the structure of an SMTP message.</span></span>
  
<span data-ttu-id="3ba8b-108">Die TNEF-Implementierung definiert mehrere TNEF-spezifische Attribute, von die jedes eine bestimmte MAPI-Eigenschaft entspricht.</span><span class="sxs-lookup"><span data-stu-id="3ba8b-108">The TNEF implementation defines several TNEF-specific attributes, each of which corresponds to a particular MAPI property.</span></span> <span data-ttu-id="3ba8b-109">Diese Attribute werden verwendet, um ihre jeweiligen MAPI-Eigenschaften in die TNEF-Stream codieren.</span><span class="sxs-lookup"><span data-stu-id="3ba8b-109">These attributes are used to encode their respective MAPI properties into the TNEF stream.</span></span> <span data-ttu-id="3ba8b-110">Darüber hinaus ist ein spezielles Attribut definiert, die zum Kapseln von MAPI-Eigenschaften, die ein bestimmtes Attribut, es entspricht nicht verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="3ba8b-110">In addition, a special attribute is defined that can be used to encapsulate any MAPI property that does not have a specific attribute corresponding to it.</span></span> <span data-ttu-id="3ba8b-111">Der Grund dafür, diese Attribute definiert werden – anstatt einfach eine einheitliche Codierungsverfahren für alle MAPI-Eigenschaften – Abwärtskompatibilität mit nicht-MAPI-kompatible Software zu aktivieren, die die TNEF verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3ba8b-111">The reason these attributes are defined — instead of simply using a uniform encoding method for all MAPI properties — is to enable backward compatibility with non-MAPI-compliant software that is using TNEF.</span></span>
  
<span data-ttu-id="3ba8b-112">Der Rest dieses Abschnitts wird die Struktur und Syntax von TNEF-Stream, der Zuordnung zwischen MAPI-Eigenschaften und TNEF-Attribute und wichtige Überlegungen für bestimmte TNEF-Attribute beschrieben.</span><span class="sxs-lookup"><span data-stu-id="3ba8b-112">The remainder of this section describes the structure and syntax of a TNEF stream, the mapping between MAPI properties and TNEF attributes, and important considerations for certain TNEF attributes.</span></span>
  

