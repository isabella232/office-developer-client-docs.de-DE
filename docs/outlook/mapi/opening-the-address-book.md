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
ms.openlocfilehash: 6d1a7e8e1d9debd7eb715bbe4958657c000f1e6b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326166"
---
# <a name="opening-the-address-book"></a>Öffnen des Adressbuchs

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Call [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) to open the integrated address book and retrieve a pointer to the MAPI [IAddrBook: IMAPIProp](iaddrbookimapiprop.md) interface. The methods of the **IAddrBook** interface can be used to access entries in all of the containers of each of the address book providers in the profile. 
  
**OpenAddressBook** might return a warning, MAPI_W_ERRORS_RETURNED, to indicate that there were problems with one or more of the address book providers. Interactive clients should call [IMAPISession::GetLastError](imapisession-getlasterror.md) to retrieve additional error information and display the returned information the first time they call **OpenAddressBook** and it returns a warning. 
  
Nicht interaktive Clients sollte ignorieren Sie die Warnung und fortgesetzt werden, als wenn die Methode erfolgreich ausgef�hrt wurde. Die zur�ckgegebene **IAddrBook** -Schnittstelle ist g�ltig, unabh�ngig davon, ob alle, einige oder keine der im Profil der adressbuchanbietern implementierte ausgef�hrt werden. Aus diesem Grund m�ssen interaktiven und nicht interaktiven Clients stets den Zeiger **IAddrBook** freigeben, wenn die Sitzung beendet. 
  

