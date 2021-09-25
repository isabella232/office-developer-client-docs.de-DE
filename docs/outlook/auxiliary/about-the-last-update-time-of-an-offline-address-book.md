---
title: Informationen zum Zeitpunkt letzten Aktualisierung des eines Offlineadressbuchs
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: d8c554c5-89ac-9b32-5561-8d8178d2525a
description: Ein Offlineadressbuch (OAB) stellt Outlook-Benutzer in einem getrennten Status Zugriff auf Verzeichnisinformationen aus der globalen Adressliste (GAL) und aus anderen Adressbüchern bereit.
ms.openlocfilehash: 57904298c0265585e4613c4f2a7f4dd466cedd7b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592830"
---
# <a name="about-the-last-update-time-of-an-offline-address-book"></a>Informationen zum Zeitpunkt letzten Aktualisierung des eines Offlineadressbuchs

Ein Offlineadressbuch (OAB) stellt Outlook-Benutzer in einem getrennten Status Zugriff auf Verzeichnisinformationen aus der globalen Adressliste (GAL) und aus anderen Adressbüchern bereit. Es wird eine Kopie der ein Adressbuch, die von einem Exchange-Server offline zugreifen Outlook heruntergeladen wurde.
  
Exchange-Administratoren können auswählen, welche Adressbücher für Benutzer verfügbar machen, die offline arbeiten. Exchange um eine Kopie der ein Adressbuch zu erstellen, neue OAB-Dateien generiert, komprimiert die Dateien und platziert sie in einer lokalen Freigabe. Abhängig davon, wie Outlook konfiguriert ist wird die OAB-Dateien aus dem Web oder in einem öffentlichen Ordner auf einem Clientcomputer für getrennt Verwenden von Outlook heruntergeladen. Outlook in regelmäßigen Abständen überprüft und lädt OAB-Updates.
  
Outlook-Lösungen, die die Benutzer offline-Zugriff auf ein OAB bereitstellen möchten, müssen möglicherweise ermitteln, wann das OAB aus dem Exchange-Server zuletzt aktualisiert wurde. Zeitpunkt der letzten Aktualisierung eines OAB verwenden, um Lösungen können den folgenden Eintrag in der Windows-Registrierung: **HKCU\Software\Microsoft\Exchange\Exchange Provider\OAB zuletzt aktualisiert**. Der Typ dieses Registrierungseintrags ist **REG_BINARY**. Die Daten sind 8 Bytes groß. Konvertieren Sie die Daten in eine 64-Bit- [FILETIME](https://msdn.microsoft.com/library/9baf8a0e-59e3-4fbd-9616-2ec9161520d1%28Office.15%29.aspx) -Struktur, die Angabe eines Wertes koordinierte Weltzeit (UTC), dass Outlook zuletzt die OAB-Dateien vom Exchange-Server auf den Clientcomputer heruntergeladen haben. 
  
## <a name="see-also"></a>Siehe auch

- [Managing Offline Address Books](https://msdn.microsoft.com/library/b7f26eca-b93b-4834-ba50-11febdefbb18.aspx)

