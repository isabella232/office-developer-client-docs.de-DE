---
title: Informationen zum Festlegen der Auflösungsreihenfolge für Adresslisten in Outlook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e1589568-cb49-86dd-5d16-b08c8117bd17
description: 'Letzte Änderung: 05. Juli 2012'
ms.openlocfilehash: 07a4c3e90f686f291f95ff87f337b54d8bf35edc
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391409"
---
# <a name="about-setting-the-resolution-order-for-address-lists-in-outlook"></a><span data-ttu-id="4c966-103">Informationen zum Festlegen der Auflösungsreihenfolge für Adresslisten in Outlook</span><span class="sxs-lookup"><span data-stu-id="4c966-103">About Setting the Resolution Order for Address Lists in Outlook</span></span>

  
  
<span data-ttu-id="4c966-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4c966-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4c966-105">Für jedes Profil unterstützt Microsoft Office Outlook mehrere Adresslisten, und Benutzer können die Reihenfolge der Adresslisten angeben, anhand der Empfänger in E-Mail-Nachrichten und Teilnehmer in Besprechungsanfragen aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="4c966-105">For each profile, Microsoft Office Outlook supports multiple address lists and users can manually specify the order of address lists by which recipients in e-mail messages and attendees in meeting requests are resolved.</span></span> <span data-ttu-id="4c966-106">Sie können beispielsweise die Auflösungsreihenfolge so festlegen, dass Namen zuerst anhand des Outlook-Adressbuchs und dann anhand der globalen Adressliste aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="4c966-106">For example, you can set the resolution order so that names are resolved first against your Outlook Address Book, and then against the Global Address List.</span></span> <span data-ttu-id="4c966-107">Auf einem Computer kann ein Benutzer das Adressbuch öffnen, und dann auf **Extras** und **Optionen** klicken, um die Auflösungsreihenfolge anzugeben.</span><span class="sxs-lookup"><span data-stu-id="4c966-107">On a computer, a user can open the Address Book, click **Tools** and then **Options** to specify this resolution order.</span></span> <span data-ttu-id="4c966-108">In einer Unternehmensumgebung ist es für IT-Administratoren jedoch effizienter, die Reihenfolge von Adresslisten, anhand der Namen aufgelöst werden, programmgesteuert festzulegen.</span><span class="sxs-lookup"><span data-stu-id="4c966-108">However, in a corporate environment, it is more efficient for IT administrators to programmatically set the order of address lists by which names are resolved.</span></span> <span data-ttu-id="4c966-109">Diese Art von Code kann als Teil eines Skripts zum Starten Automation verwendet werden, die von ein Administrator innerhalb des Unternehmens bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="4c966-109">Such code can be used as part of a startup automation script that an administrator deploys inside the corporation.</span></span> 
  
<span data-ttu-id="4c966-p102">MAPI unterstützt die **[SetSearchPath](iaddrbook-getsearchpath.md)**-Methode in der **[IAddrBook](iaddrbookimapiprop.md)**-Schnittstelle, sodass Sie einen neuen Suchpfad in dem Profil festlegen können, der für die Namensauflösung verwendet wird. Um die **IAddrBook::SetSearchPath**-Methode zu verwenden, müssen Sie die gewünschte Auflösungsreihenfolge mithilfe eines Arrays angeben, das Container der relevanten Adressbücher in der Reihenfolge enthält, in der diese aufgelöst werden sollten. Jeder Eintrag in diesem Array sollte auch die Eintrags-ID des entsprechenden Adressbuchs enthalten.</span><span class="sxs-lookup"><span data-stu-id="4c966-p102">MAPI supports the **[SetSearchPath](iaddrbook-getsearchpath.md)** method in the **[IAddrBook](iaddrbookimapiprop.md)** interface, which allows you to set a new search path in the profile that is used for name resolution. To use the **IAddrBook::SetSearchPath** method, you must specify the desired resolution order by using an array that holds containers of the relevant address books in the order they should be resolved. Each entry in that array should also contain the entry ID of the corresponding address book.</span></span> 
  
<span data-ttu-id="4c966-113">Nachfolgend finden Sie Codebeispiele dafür, wie ein benutzerdefinierter Suchpfad für Adresslisten angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="4c966-113">The following are code examples of how to specify a custom search path for address lists.</span></span>
  
- [<span data-ttu-id="4c966-114">Programmgesteuertes Festlegen der Auflösungsreihenfolge für Adresslisten</span><span class="sxs-lookup"><span data-stu-id="4c966-114">Programmatically set the resolution order for address lists</span></span>](how-to-programmatically-set-the-resolution-order-for-address-lists.md)
    
- [<span data-ttu-id="4c966-115">KB 292590: Ändern der Adressbuch-Sortierreihenfolge mit SetSearchPath</span><span class="sxs-lookup"><span data-stu-id="4c966-115">KB 292590: How To Change Address Book Sort Order with SetSearchPath</span></span>](https://support.microsoft.com/kb/292590)
    

