---
title: Implementieren einer Container-einmal Tabelle
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eabbde74-49a1-4eeb-a01d-67e45ae4b343
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 72dc73b6ed8519be2d8010544fdd5dc5b7b0f759
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332886"
---
# <a name="implementing-a-container-one-off-table"></a><span data-ttu-id="acfae-103">Implementieren einer Container-einmal Tabelle</span><span class="sxs-lookup"><span data-stu-id="acfae-103">Implementing a Container One-Off Table</span></span>

  
  
<span data-ttu-id="acfae-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="acfae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="acfae-105">Um auf die einmalige Tabelle zuzugreifen, die zu einem ihrer Container gehört, ruft MAPI die [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Methode des Containers auf, um die **PR_CREATE_TEMPLATES** ([pidtagcreatetemplates (](pidtagcreatetemplates-canonical-property.md))-Eigenschaft mit der **IMAPITable** zu öffnen. Oberfläche.</span><span class="sxs-lookup"><span data-stu-id="acfae-105">To access the one-off table belonging to one of your containers, MAPI calls the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property with the **IMAPITable** interface.</span></span> <span data-ttu-id="acfae-106">Der Container wird aufgefordert, seine einmalige Tabelle zurückzugeben, wenn eine Clientanwendung versucht, dem Container einen Empfänger hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="acfae-106">Your container is asked to return its one-off table when a client application is trying to add a recipient to the container.</span></span> <span data-ttu-id="acfae-107">Wenn der Container Empfänger zulässt, kann Ihr Anbieter entweder eine eigene Tabellen Implementierung zurückgeben oder [IMAPISupport:: GetOneOffTable](imapisupport-getoneofftable.md) aufrufen, um die MAPI-Implementierung zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="acfae-107">If the container allows any recipients, your provider can either return its own table implementation or call [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md) to return the MAPI implementation.</span></span> 
  
<span data-ttu-id="acfae-108">Der Vorlagensatz in der einmaligen Container Tabelle sollte den Typ der Empfänger widerspiegeln, die der jeweilige Container enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="acfae-108">The set of templates in the container one-off table should reflect the type of recipients that the particular container can hold.</span></span> <span data-ttu-id="acfae-109">Dies umfasst in der Regel eine oder zwei Vorlagen, Vorlagen zum Erstellen eines einzelnen Messaging Benutzers oder einer Verteilerliste.</span><span class="sxs-lookup"><span data-stu-id="acfae-109">Typically, this includes one or two templates, templates for creating an individual messaging user or a distribution list.</span></span> <span data-ttu-id="acfae-110">Die Eintragsbezeichner für diese Vorlagen werden in den Eigenschaften **PR_DEF_CREATE_MAILUSER** ([Pidtagdefcreatemailuser (](pidtagdefcreatemailuser-canonical-property.md)) und **PR_DEF_CREATE_DL** ([pidtagdefcreatedl (](pidtagdefcreatedl-canonical-property.md)) gespeichert.</span><span class="sxs-lookup"><span data-stu-id="acfae-110">The entry identifiers for these templates are held in the **PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) and **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)) properties.</span></span> <span data-ttu-id="acfae-111">Container sind jedoch keineswegs auf diese Art von Einträgen beschränkt.</span><span class="sxs-lookup"><span data-stu-id="acfae-111">However, containers are by no means limited to these types of entries.</span></span> <span data-ttu-id="acfae-112">Sie können andere Typen von Empfängern oder nicht Empfänger Einträgen wie Verzeichnissen enthalten.</span><span class="sxs-lookup"><span data-stu-id="acfae-112">They can hold other types of recipients or non-recipient entries such as directories.</span></span> 
  

