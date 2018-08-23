---
title: Öffnen des Adressbuchs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79e0bc93-f37d-4f6a-beed-7519d01e0056
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 62a4e6a09570cc3d71b0797ed7fff162d05ee416
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583687"
---
# <a name="opening-the-address-book"></a><span data-ttu-id="ca756-103">Öffnen des Adressbuchs</span><span class="sxs-lookup"><span data-stu-id="ca756-103">Opening the address book</span></span>

<span data-ttu-id="ca756-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ca756-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ca756-p101">Call [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) to open the integrated address book and retrieve a pointer to the MAPI [IAddrBook: IMAPIProp](iaddrbookimapiprop.md) interface. The methods of the **IAddrBook** interface can be used to access entries in all of the containers of each of the address book providers in the profile.</span><span class="sxs-lookup"><span data-stu-id="ca756-p101">Call [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) to open the integrated address book and retrieve a pointer to the MAPI [IAddrBook : IMAPIProp](iaddrbookimapiprop.md) interface. The methods of the **IAddrBook** interface can be used to access entries in all of the containers of each of the address book providers in the profile.</span></span> 
  
<span data-ttu-id="ca756-p102">**OpenAddressBook** might return a warning, MAPI_W_ERRORS_RETURNED, to indicate that there were problems with one or more of the address book providers. Interactive clients should call [IMAPISession::GetLastError](imapisession-getlasterror.md) to retrieve additional error information and display the returned information the first time they call **OpenAddressBook** and it returns a warning.</span><span class="sxs-lookup"><span data-stu-id="ca756-p102">**OpenAddressBook** might return a warning, MAPI_W_ERRORS_RETURNED, to indicate that there were problems with one or more of the address book providers. Interactive clients should call [IMAPISession::GetLastError](imapisession-getlasterror.md) to retrieve additional error information and display the returned information the first time they call **OpenAddressBook** and it returns a warning.</span></span> 
  
<span data-ttu-id="ca756-p103">Nicht interaktive Clients sollte ignorieren Sie die Warnung und fortgesetzt werden, als wenn die Methode erfolgreich ausgef�hrt wurde. Die zur�ckgegebene **IAddrBook** -Schnittstelle ist g�ltig, unabh�ngig davon, ob alle, einige oder keine der im Profil der adressbuchanbietern implementierte ausgef�hrt werden. Aus diesem Grund m�ssen interaktiven und nicht interaktiven Clients stets den Zeiger **IAddrBook** freigeben, wenn die Sitzung beendet.</span><span class="sxs-lookup"><span data-stu-id="ca756-p103">Noninteractive clients should ignore the warning and proceed as if the method succeeded. The returned **IAddrBook** interface is valid regardless of whether all, some, or none of the address book providers in the profile are running. Therefore, both interactive and noninteractive clients must always remember to release the **IAddrBook** pointer when the session ends.</span></span> 
  

