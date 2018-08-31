---
title: Integration in Office von Win32-Synchronisierungsclients aus
manager: soliver
ms.date: 07/29/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 348555d3-3cd4-4e4a-b5ad-436571c25251
description: Integrieren Sie Ihre Drittanbieter-Win32-Synchronisierungsclients mit Excel Mobile-, PowerPoint Mobile- und Word Mobile-Office-Anwendungen.
ms.openlocfilehash: 9f520ad36583a9aa7cd73638fe92158f70d13daf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790858"
---
# <a name="integrate-with-office-from-win32-sync-clients"></a>Integration in Office von Win32-Synchronisierungsclients aus

Integrieren Sie Ihre Drittanbieter-Win32-Synchronisierungsclients mit Excel Mobile-, PowerPoint Mobile- und Word Mobile-Office-Anwendungen. 
  
Sie können Ihre universelle Windows-App mit Excel Mobile-, PowerPoint Mobile- und Word Mobile-Clients integrieren, indem Sie sie als Synchronisierungsstammanbieter registrieren. In diesem Artikel werden die bewährten Methoden beschrieben, um sicherzustellen, dass Ihre Win32-Synchronisierungsclients problemlos mit Office-Anwendungen zusammenarbeiten.
  
Für diese Integration muss der Win32-Synchronisierungsclient über ein Synchronisierungsmodul verfügen.
  
## <a name="register-as-a-sync-root-provider"></a>Registrieren als Synchronisierungsstammanbieter

Wenn Ihr Synchronisierungsclient nicht als Synchronisierungsstammanbieter registriert ist, behandelt Office Dateien im Synchronisierungsordner wie normale lokale Dateien. Dies bedeutet, dass Office Benutzern Optionen wie "Zu OneDrive verschieben" anbietet, wenn sie versuchen, das Dokument freizugeben. Um dies für Dateien zu vermeiden, die Sie synchronisieren, müssen Sie die Registrierung als Synchronisierungsstammanbieter ausführen. Informationen über das Registrieren finden Sie unter [Integrieren eines Cloud-Speicheranbieters](https://msdn.microsoft.com/de-DE/library/windows/desktop/dn889934%28v=vs.85%29.aspx).
  
## <a name="integrate-your-app-into-the-root-node-of-the-navigation-pane"></a>Integrieren der App in den Stammknoten des Navigationsbereichs

Damit Ihr Win32-Synchronisierungsclient im Datei-Explorer und der Windows-Dateiauswahl als Stammknoten im Navigationsbereich angezeigt wird, müssen Sie Ihre App in die Stammebene integrieren. Weitere Informationen dazu finden Sie unter [Integrieren eines Cloud-Speicheranbieters](https://msdn.microsoft.com/de-DE/library/windows/desktop/dn889934%28v=vs.85%29.aspx). 
  
## <a name="add-your-sync-folder-as-a-document-library-optional"></a>Hinzufügen des Synchronisierungsordners als Dokumentbibliothek (optional)

In Office können Benutzer mit einer einzelnen Aktion Dokumente in ihren Dokumentbibliotheken erstellen. Um Ihren Synchronisierungsspeicherort der Dokumentbibliothek hinzuzufügen, verwenden Sie die [SHAddFolderPathToLibrary-Funktion](https://msdn.microsoft.com/de-DE/library/windows/desktop/dd378432%28v=vs.85%29.aspx). 
  
## <a name="see-also"></a>Siehe auch
<a name="bk_addresources"> </a>

- [Integration in Office](integrate-with-office.md)
    
- [Integration in Office von universellen Windows-Apps aus](integrate-with-office-from-windows-universal-apps.md)
    

