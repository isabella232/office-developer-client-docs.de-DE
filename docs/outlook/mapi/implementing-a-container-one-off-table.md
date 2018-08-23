---
title: Implementieren einer Container-Einmaltabelle
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eabbde74-49a1-4eeb-a01d-67e45ae4b343
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d468943f84f1d23f1b4b84881e69cee0041a5bae
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576596"
---
# <a name="implementing-a-container-one-off-table"></a><span data-ttu-id="972f4-103">Implementieren einer Container-Einmaltabelle</span><span class="sxs-lookup"><span data-stu-id="972f4-103">Implementing a Container One-Off Table</span></span>

  
  
<span data-ttu-id="972f4-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="972f4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="972f4-105">Zugriff auf die einmalige Tabelle einer von Ihrer Containern MAPI des Containers [IMAPIProp::OpenProperty](imapiprop-openproperty.md) -Methode zum Öffnen der **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md))-Eigenschaft mit der **IMAPITable** aufgerufen Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="972f4-105">To access the one-off table belonging to one of your containers, MAPI calls the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property with the **IMAPITable** interface.</span></span> <span data-ttu-id="972f4-106">Der Container wird gefragt, seine einmalige Tabelle zurückzugeben, wenn eine Clientanwendung versucht, einen Empfänger an den Container hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="972f4-106">Your container is asked to return its one-off table when a client application is trying to add a recipient to the container.</span></span> <span data-ttu-id="972f4-107">Wenn der Container Empfänger zulässt, kann vom Dienstanbieter entweder eine eigene Tabelle-Implementierung zurückzugeben oder [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md) , um die MAPI-Implementierung zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="972f4-107">If the container allows any recipients, your provider can either return its own table implementation or call [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md) to return the MAPI implementation.</span></span> 
  
<span data-ttu-id="972f4-108">Die Gruppe der Vorlagen in der einmaligen Container-Tabelle sollte den Typ der Empfänger wieder, die der jeweiligen Container enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="972f4-108">The set of templates in the container one-off table should reflect the type of recipients that the particular container can hold.</span></span> <span data-ttu-id="972f4-109">Dies umfasst in der Regel ein oder zwei Vorlagen, Vorlagen für die Erstellung einer einzelnen messaging-Benutzer oder eine Verteilerliste.</span><span class="sxs-lookup"><span data-stu-id="972f4-109">Typically, this includes one or two templates, templates for creating an individual messaging user or a distribution list.</span></span> <span data-ttu-id="972f4-110">Für diese Vorlagen den Eintrag-IDs werden in die **PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) und **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)) Eigenschaften gehalten.</span><span class="sxs-lookup"><span data-stu-id="972f4-110">The entry identifiers for these templates are held in the **PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) and **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)) properties.</span></span> <span data-ttu-id="972f4-111">Container sind jedoch nicht auf diese Arten von Einträgen beschränkt.</span><span class="sxs-lookup"><span data-stu-id="972f4-111">However, containers are by no means limited to these types of entries.</span></span> <span data-ttu-id="972f4-112">Sie können andere Typen von Empfängern oder nicht-Recipient Einträge wie Verzeichnisse enthalten.</span><span class="sxs-lookup"><span data-stu-id="972f4-112">They can hold other types of recipients or non-recipient entries such as directories.</span></span> 
  

