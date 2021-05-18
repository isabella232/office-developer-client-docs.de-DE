---
title: Informationen zum Festlegen der L�sung Reihenfolge f�r Adresslisten in Outlook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e1589568-cb49-86dd-5d16-b08c8117bd17
description: 'Letzte Änderung: 05. Juli 2012'
ms.openlocfilehash: 07a4c3e90f686f291f95ff87f337b54d8bf35edc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321833"
---
# <a name="about-setting-the-resolution-order-for-address-lists-in-outlook"></a><span data-ttu-id="eb627-103">Informationen zum Festlegen der Auflösungsreihenfolge für Adresslisten in Outlook</span><span class="sxs-lookup"><span data-stu-id="eb627-103">About Setting the Resolution Order for Address Lists in Outlook</span></span>

  
  
<span data-ttu-id="eb627-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eb627-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eb627-105">Für jedes Profil unterstützt Microsoft Office Outlook mehrere Adresslisten, und Benutzer können die Reihenfolge der Adresslisten angeben, anhand der Empfänger in E-Mail-Nachrichten und Teilnehmer in Besprechungsanfragen aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="eb627-105">For each profile, Microsoft Office Outlook supports multiple address lists and users can manually specify the order of address lists by which recipients in email messages and attendees in meeting requests are resolved.</span></span> <span data-ttu-id="eb627-106">Sie können beispielsweise die Auflösungsreihenfolge so festlegen, dass Namen zuerst anhand des Outlook-Adressbuchs und dann anhand der globalen Adressliste aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="eb627-106">For example, you can set the resolution order so that names are resolved first against your Outlook Address Book, and then against the Global Address List.</span></span> <span data-ttu-id="eb627-107">Auf einem Computer ein Benutzer im Adressbuch �ffnen, klicken Sie auf **Extras** und dann auf **Optionen**, um diesen Auftrag L�sung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="eb627-107">On a computer, a user can open the Address Book, click **Tools** and then **Options** to specify this resolution order.</span></span> <span data-ttu-id="eb627-108">Es ist jedoch in einer Unternehmensumgebung effizienter f�r IT-Administratoren die Reihenfolge der Adresslisten programmgesteuert festgelegt mit dem Namen aufgel�st werden.</span><span class="sxs-lookup"><span data-stu-id="eb627-108">However, in a corporate environment, it is more efficient for IT administrators to programmatically set the order of address lists by which names are resolved.</span></span> <span data-ttu-id="eb627-109">Diese Art von Code kann als Teil eines Skripts zum Starten Automation verwendet werden, die von ein Administrator innerhalb des Unternehmens bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="eb627-109">Such code can be used as part of a startup automation script that an administrator deploys inside the corporation.</span></span> 
  
<span data-ttu-id="eb627-p102">MAPI unterstützt die **[SetSearchPath](iaddrbook-getsearchpath.md)**-Methode in der **[IAddrBook](iaddrbookimapiprop.md)**-Schnittstelle, sodass Sie einen neuen Suchpfad in dem Profil festlegen können, der für die Namensauflösung verwendet wird. Um die **IAddrBook::SetSearchPath**-Methode zu verwenden, müssen Sie die gewünschte Auflösungsreihenfolge mithilfe eines Arrays angeben, das Container der relevanten Adressbücher in der Reihenfolge enthält, in der diese aufgelöst werden sollten. Jeder Eintrag in diesem Array sollte auch die Eintrags-ID des entsprechenden Adressbuchs enthalten.</span><span class="sxs-lookup"><span data-stu-id="eb627-p102">MAPI supports the **[SetSearchPath](iaddrbook-getsearchpath.md)** method in the **[IAddrBook](iaddrbookimapiprop.md)** interface, which allows you to set a new search path in the profile that is used for name resolution. To use the **IAddrBook::SetSearchPath** method, you must specify the desired resolution order by using an array that holds containers of the relevant address books in the order they should be resolved. Each entry in that array should also contain the entry ID of the corresponding address book.</span></span> 
  
<span data-ttu-id="eb627-113">Nachfolgend finden Sie Codebeispiele dafür, wie ein benutzerdefinierter Suchpfad für Adresslisten angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="eb627-113">The following are code examples of how to specify a custom search path for address lists.</span></span>
  
- [<span data-ttu-id="eb627-114">Programmgesteuertes Festlegen der Auflösungsreihenfolge für Adresslisten</span><span class="sxs-lookup"><span data-stu-id="eb627-114">Programmatically Set the Resolution Order for Address Lists</span></span>](how-to-programmatically-set-the-resolution-order-for-address-lists.md)
    
- [<span data-ttu-id="eb627-115">KB 292590: Ändern der Adressbuch-Sortierreihenfolge mit SetSearchPath</span><span class="sxs-lookup"><span data-stu-id="eb627-115">KB 292590: How To Change Address Book Sort Order with SetSearchPath</span></span>](https://support.microsoft.com/kb/292590)
    

