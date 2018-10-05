---
title: Informationen zum Registrieren von Stores für die Indizierung
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: dd2aa06a-96e8-1291-18b5-fc3c40b74e4d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 96322d12b3b7b334b5f78f81910dcf34c3fc78e1
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386530"
---
# <a name="about-registering-stores-for-indexing"></a>Informationen zum Registrieren von Stores für die Indizierung

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
In diesem Thema wird speziell für die Sofortsuche in Microsoft Office Outlook 2007.
  
Sofortsuche können Sie die Elemente in Outlook schnell finden. Komponenten der Windows-Desktopsuche verwendet.
  
Der MAPI-Protokollhandler überprüft die Windows-Registrierung für Geschäfte, die indiziert werden soll für die Suche. Speicheranbieter, die indiziert werden soll, müssen in der Windows-Registrierung registriert werden.
  
Standardmäßig wird der Windows-Registrierung zu indizieren mit Windows-Desktopsuche die folgenden vier Typen von Anbietern hinzugefügt:
  
- Speicher für Persönliche Ordner-Dateien (. PST).
    
-  Microsoft Exchange-Speicher, einschließlich alle Offlineordnerdateien (OST). 
    
-  Informationsspeicher für Öffentliche Ordner. 
    
-  Anmelden für Microsoft Office Outlook Connector für MSN. 
    
 Drittanbieter-Anbieter, die indiziert werden möchten, müssen sich selbst in der Windows-Registrierung registrieren. 
  
> [!NOTE]
> Administratoren und Benutzer können eine Gruppenrichtlinie verwenden, um zu verhindern, dass Windows-Desktopsuche Indizieren von Outlook-Elementen. Weitere Informationen finden Sie unter [Windows-Desktopsuche erweitern](https://msdn.microsoft.com/library/2eab146a-8516-4b95-b73c-ca7f980ba233%28Office.15%29.aspx). 
  
## <a name="registry-keys"></a>Registrierungsschlüssel

Auf einem Computer müssen alle Speicher-Anbieter, die indiziert werden soll, unter nur einer der folgenden drei Registrierungsschlüssel in der Windows-Registrierung registriert werden. Der MAPI-Protokollhandler sieht unter jeder dieser Schlüssel in der folgenden Reihenfolge:
  
1. \Software\Policies\Microsoft\Windows\Windows Search\ [HKLM]
    
2. \Software\Microsoft\Windows\Windows Search\Preferences\ [HKLM]
    
3. \Software\Microsoft\Windows\Windows Search\Preferences\ [HKCU]
    
 Jeder Wert unter dem Schlüssel entspricht einem Anbieter, der indiziert werden würde. Der Name des Werts ist die GUID (GLOBALLY Unique Identifier) des Anbieters, die vom Typ **DWORD-Wert** und den Hexadezimalwert 0 x 00000001 hat. 
  
## <a name="guids-for-store-providers"></a>GUIDs für Anbieter

Die MAPI-Eigenschaft **[PR_MDB_PROVIDER](pidtagstoreprovider-canonical-property.md)** gibt die GUID der MAPI-Speicher. Die GUIDs für den Anbieter, dass Outlook Indizes in der folgenden Tabelle beschrieben werden. 
  
||||
|:-----|:-----|:-----|
|**Typ des Anbieters** <br/> |**GUID** <br/> |**Hinweise** <br/> |
|Persönliche Ordner-Dateien (. PST)  <br/> |{4154494E-BFF9-01B8-00AA-0037D96E0000}  <br/> |GUID wird in der öffentlichen Header Datei mspst.h als **MSPST_UID_PROVIDER** dokumentiert. <br/> |
|Exchange  <br/> |{C0A19454-7F29-1B10-A587-08002B2A2517}  <br/> |GUID wird in der öffentlichen Header Datei edkmdb.h als **PbExchangeProviderPrimaryUserGuid** dokumentiert. <br/> |
|Öffentliche Ordner  <br/> |{70fab278-f7af-cd11-9bc8-00aa002fc45a}  <br/> |GUID wird in der öffentlichen Header Datei edkmdb.h als **PbExchangeProviderPublicGuid** dokumentiert. <br/> |
|Outlook Connector für MSN  <br/> |{c34f5c97-eb05-bb4b-b199-2a7570ec7cf9}  <br/> |Keine  <br/> |
   
## <a name="see-also"></a>Siehe auch



[Informationen zur Store-API](about-the-store-api.md)

