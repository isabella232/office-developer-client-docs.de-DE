---
title: Informationen zum Zeitpunkt letzten Aktualisierung des eines Offlineadressbuchs
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: d8c554c5-89ac-9b32-5561-8d8178d2525a
description: Ein Offlineadressbuch (OAB) stellt Outlook-Benutzer in einem getrennten Status Zugriff auf Verzeichnisinformationen aus der globalen Adressliste (GAL) und aus anderen Adressbüchern bereit.
ms.openlocfilehash: 3374f87cd62d46a80ed823bff0516115a58c155c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317017"
---
# <a name="about-the-last-update-time-of-an-offline-address-book"></a><span data-ttu-id="d4255-103">Informationen zum Zeitpunkt letzten Aktualisierung des eines Offlineadressbuchs</span><span class="sxs-lookup"><span data-stu-id="d4255-103">About the last update time of an Offline Address Book</span></span>

<span data-ttu-id="d4255-p101">Ein Offlineadressbuch (OAB) stellt Outlook-Benutzer in einem getrennten Status Zugriff auf Verzeichnisinformationen aus der globalen Adressliste (GAL) und aus anderen Adressbüchern bereit. Es wird eine Kopie der ein Adressbuch, die von einem Exchange-Server offline zugreifen Outlook heruntergeladen wurde.</span><span class="sxs-lookup"><span data-stu-id="d4255-p101">An Offline Address Book (OAB) provides Outlook users in a disconnected state access to directory information from the Global Address List (GAL) and from other address books. It is a copy of an Address Book that Outlook has downloaded from an Exchange server to provide offline access.</span></span>
  
<span data-ttu-id="d4255-p102">Exchange-Administratoren können auswählen, welche Adressbücher für Benutzer verfügbar machen, die offline arbeiten. Exchange um eine Kopie der ein Adressbuch zu erstellen, neue OAB-Dateien generiert, komprimiert die Dateien und platziert sie in einer lokalen Freigabe. Abhängig davon, wie Outlook konfiguriert ist wird die OAB-Dateien aus dem Web oder in einem öffentlichen Ordner auf einem Clientcomputer für getrennt Verwenden von Outlook heruntergeladen. Outlook in regelmäßigen Abständen überprüft und lädt OAB-Updates.</span><span class="sxs-lookup"><span data-stu-id="d4255-p102">Exchange administrators can choose which Address Books to make available for users who work offline. To create a copy of an Address Book, Exchange generates new OAB files, compresses the files, and places them on a local share. Depending on how Outlook is configured, Outlook downloads the OAB files either from the Web or from a Public Folder to a client computer for use in a disconnected state. Outlook periodically checks for and downloads OAB updates.</span></span>
  
<span data-ttu-id="d4255-p103">Outlook-Lösungen, die die Benutzer offline-Zugriff auf ein OAB bereitstellen möchten, müssen möglicherweise ermitteln, wann das OAB aus dem Exchange-Server zuletzt aktualisiert wurde. Zeitpunkt der letzten Aktualisierung eines OAB verwenden, um Lösungen können den folgenden Eintrag in der Windows-Registrierung: **HKCU\Software\Microsoft\Exchange\Exchange Provider\OAB zuletzt aktualisiert**. Der Typ dieses Registrierungseintrags ist **REG_BINARY**. Die Daten sind 8 Bytes groß. Konvertieren Sie die Daten in eine 64-Bit- [FILETIME](https://msdn.microsoft.com/library/9baf8a0e-59e3-4fbd-9616-2ec9161520d1%28Office.15%29.aspx) -Struktur, die Angabe eines Wertes koordinierte Weltzeit (UTC), dass Outlook zuletzt die OAB-Dateien vom Exchange-Server auf den Clientcomputer heruntergeladen haben.</span><span class="sxs-lookup"><span data-stu-id="d4255-p103">Outlook solutions that want to provide their users offline access to an OAB may need to find out when the OAB was last updated from the Exchange server. To find the last update time of an OAB, solutions can use the following entry in the Windows registry: **HKCU\Software\Microsoft\Exchange\Exchange Provider\OAB Last Modified Time**. The type of this registry entry is **REG_BINARY**. The data is 8 bytes in size. You can convert the data to a 64-bit [FILETIME](https://msdn.microsoft.com/library/9baf8a0e-59e3-4fbd-9616-2ec9161520d1%28Office.15%29.aspx) structure specifying a Universal Coordinated Time (UTC) value that Outlook last downloaded the OAB files from the Exchange server to the client computer.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d4255-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d4255-115">See also</span></span>

- [<span data-ttu-id="d4255-116">Managing Offline Address Books</span><span class="sxs-lookup"><span data-stu-id="d4255-116">Managing Offline Address Books</span></span>](https://msdn.microsoft.com/library/b7f26eca-b93b-4834-ba50-11febdefbb18.aspx)

