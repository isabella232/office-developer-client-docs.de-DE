---
title: Informationen zum Festlegen der L�sung Reihenfolge f�r Adresslisten in Outlook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e1589568-cb49-86dd-5d16-b08c8117bd17
description: 'Letzte �nderung: Donnerstag, 5. Juli 2012'
ms.openlocfilehash: 22d56ffac5d9d628b04e364fa772ddc8de488a31
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578654"
---
# <a name="about-setting-the-resolution-order-for-address-lists-in-outlook"></a><span data-ttu-id="c4d21-103">Informationen zum Festlegen der L�sung Reihenfolge f�r Adresslisten in Outlook</span><span class="sxs-lookup"><span data-stu-id="c4d21-103">About Setting the Resolution Order for Address Lists in Outlook</span></span>

  
  
<span data-ttu-id="c4d21-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c4d21-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c4d21-105">Für jedes Profil Microsoft Office Outlook unterstützt mehrere Adresslisten, und Benutzer können die Reihenfolge der Adresslisten, die von der, die Empfänger in e-Mail-Nachrichten und Teilnehmer in Besprechungsanfragen aufgelöst werden manuell angeben.</span><span class="sxs-lookup"><span data-stu-id="c4d21-105">For each profile, Microsoft Office Outlook supports multiple address lists and users can manually specify the order of address lists by which recipients in email messages and attendees in meeting requests are resolved.</span></span> <span data-ttu-id="c4d21-106">Beispielsweise k�nnen Sie die Reihenfolge der L�sung festlegen, sodass Namen aufgel�st zuerst gegen Ihr Outlook-Adressbuch, und klicken Sie dann der globalen Adressliste enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="c4d21-106">For example, you can set the resolution order so that names are resolved first against your Outlook Address Book, and then against the Global Address List.</span></span> <span data-ttu-id="c4d21-107">Auf einem Computer ein Benutzer im Adressbuch �ffnen, klicken Sie auf **Extras** und dann auf **Optionen**, um diesen Auftrag L�sung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="c4d21-107">On a computer, a user can open the Address Book, click **Tools** and then **Options** to specify this resolution order.</span></span> <span data-ttu-id="c4d21-108">Es ist jedoch in einer Unternehmensumgebung effizienter f�r IT-Administratoren die Reihenfolge der Adresslisten programmgesteuert festgelegt mit dem Namen aufgel�st werden.</span><span class="sxs-lookup"><span data-stu-id="c4d21-108">However, in a corporate environment, it is more efficient for IT administrators to programmatically set the order of address lists by which names are resolved.</span></span> <span data-ttu-id="c4d21-109">Diese Art von Code kann als Teil eines Skripts zum Starten Automation verwendet werden, die von ein Administrator innerhalb des Unternehmens bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="c4d21-109">Such code can be used as part of a startup automation script that an administrator deploys inside the corporation.</span></span> 
  
<span data-ttu-id="c4d21-p102">MAPI unterst�tzt die **[SetSearchPath](iaddrbook-getsearchpath.md)** -Methode in die **[IAddrBook](iaddrbookimapiprop.md)** -Schnittstelle k�nnen Sie einen neuen Pfad f�r die Suche im Profil festlegen, die f�r die Namensaufl�sung verwendet wird. Wie die **IAddrBook::SetSearchPath** -Methode verwenden, m�ssen Sie angeben, auf die gew�nschte Aufl�sung Reihenfolge unter Verwendung eines Arrays, das Container f�r die entsprechende Adresse enth�lt in der Reihenfolge von Adressb�chern, die sie gel�st werden sollen. Jeder Eintrag in diesem Array sollte auch die Eintrags-ID des entsprechenden Adressbuch enthalten.</span><span class="sxs-lookup"><span data-stu-id="c4d21-p102">MAPI supports the **[SetSearchPath](iaddrbook-getsearchpath.md)** method in the **[IAddrBook](iaddrbookimapiprop.md)** interface, which allows you to set a new search path in the profile that is used for name resolution. To use the **IAddrBook::SetSearchPath** method, you must specify the desired resolution order by using an array that holds containers of the relevant address books in the order they should be resolved. Each entry in that array should also contain the entry ID of the corresponding address book.</span></span> 
  
<span data-ttu-id="c4d21-113">Es folgen Beispiele daf�r, wie Sie eine benutzerdefinierte Suchpfad f�r Adresslisten an Code.</span><span class="sxs-lookup"><span data-stu-id="c4d21-113">The following are code examples of how to specify a custom search path for address lists.</span></span>
  
- [<span data-ttu-id="c4d21-114">Programmgesteuertes Festlegen der Lösungsreihenfolge für Adresslisten</span><span class="sxs-lookup"><span data-stu-id="c4d21-114">Programmatically Set the Resolution Order for Address Lists</span></span>](how-to-programmatically-set-the-resolution-order-for-address-lists.md)
    
- [<span data-ttu-id="c4d21-115">KB 292590: zum �ndern der Address Book Sortierreihenfolge mit SetSearchPath</span><span class="sxs-lookup"><span data-stu-id="c4d21-115">KB 292590: How To Change Address Book Sort Order with SetSearchPath</span></span>](http://support.microsoft.com/kb/292590)
    

