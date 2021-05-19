---
title: Implementieren einer One-Off-Tabelle
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eabbde74-49a1-4eeb-a01d-67e45ae4b343
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 72dc73b6ed8519be2d8010544fdd5dc5b7b0f759
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417420"
---
# <a name="implementing-a-container-one-off-table"></a><span data-ttu-id="0048c-103">Implementieren einer One-Off-Tabelle</span><span class="sxs-lookup"><span data-stu-id="0048c-103">Implementing a Container One-Off Table</span></span>

  
  
<span data-ttu-id="0048c-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0048c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0048c-105">Um auf die einmal zu einem Ihrer Container gehörende Tabelle zu zugreifen, ruft MAPI die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) des Containers auf, um die **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md))-Eigenschaft mit der **IMAPITable-Schnittstelle** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="0048c-105">To access the one-off table belonging to one of your containers, MAPI calls the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property with the **IMAPITable** interface.</span></span> <span data-ttu-id="0048c-106">Ihr Container wird aufgefordert, seine einmal aufgeführte Tabelle zurückzukehren, wenn eine Clientanwendung versucht, dem Container einen Empfänger hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="0048c-106">Your container is asked to return its one-off table when a client application is trying to add a recipient to the container.</span></span> <span data-ttu-id="0048c-107">Wenn der Container Empfänger zulässt, kann Ihr Anbieter entweder eine eigene Tabellenimplementierung zurückgeben oder [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md) aufrufen, um die MAPI-Implementierung zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="0048c-107">If the container allows any recipients, your provider can either return its own table implementation or call [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md) to return the MAPI implementation.</span></span> 
  
<span data-ttu-id="0048c-108">Der Satz von Vorlagen in der Einmaltabelle des Containers sollte den Empfängertyp widerspiegeln, den der bestimmte Container enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="0048c-108">The set of templates in the container one-off table should reflect the type of recipients that the particular container can hold.</span></span> <span data-ttu-id="0048c-109">In der Regel umfasst dies eine oder zwei Vorlagen, Vorlagen zum Erstellen eines einzelnen Messagingbenutzers oder einer Verteilerliste.</span><span class="sxs-lookup"><span data-stu-id="0048c-109">Typically, this includes one or two templates, templates for creating an individual messaging user or a distribution list.</span></span> <span data-ttu-id="0048c-110">Die Eintragsbezeichner für diese Vorlagen werden in den **Eigenschaften PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) und **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)) enthalten.</span><span class="sxs-lookup"><span data-stu-id="0048c-110">The entry identifiers for these templates are held in the **PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) and **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)) properties.</span></span> <span data-ttu-id="0048c-111">Container sind jedoch keinesfalls auf diese Arten von Einträgen beschränkt.</span><span class="sxs-lookup"><span data-stu-id="0048c-111">However, containers are by no means limited to these types of entries.</span></span> <span data-ttu-id="0048c-112">Sie können andere Arten von Empfängern oder Nicht-Empfänger-Einträgen wie Verzeichnisse enthalten.</span><span class="sxs-lookup"><span data-stu-id="0048c-112">They can hold other types of recipients or non-recipient entries such as directories.</span></span> 
  

