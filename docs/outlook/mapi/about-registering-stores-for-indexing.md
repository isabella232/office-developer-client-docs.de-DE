---
title: Informationen zum Registrieren von Informationsspeichern für die Indizierung
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: dd2aa06a-96e8-1291-18b5-fc3c40b74e4d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e972c0a443a0c06b4df5cde5ea0ec82587d077b4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59588266"
---
# <a name="about-registering-stores-for-indexing"></a>Informationen zum Registrieren von Informationsspeichern für die Indizierung

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Dieses Thema ist spezifisch für die Sofortsuche in Microsoft Office Outlook 2007.
  
Mit der Sofortsuche können Sie Elemente in Outlook schnell finden. Es verwendet Komponenten von Windows Desktopsuche.
  
Der MAPI-Protokollhandler überprüft die Windows-Registrierung auf Speicher, die für Suchzwecke indiziert werden sollen. Store Anbieter, die indiziert werden sollen, müssen in der Windows Registrierung registriert werden.
  
Standardmäßig fügt Windows Desktopsuche der Windows Registrierung die folgenden vier Typen von Speicheranbietern hinzu, um die Indizierung zuzulassen:
  
- Store für Dateien mit persönlichen Ordnern (. PST).
    
-  Microsoft Exchange Speichern, einschließlich aller Offlineordnerdateien (OST). 
    
-  Store für öffentliche Ordner. 
    
-  Store für Microsoft Office Outlook Connector für MSN. 
    
 Drittanbieter, die indiziert werden möchten, müssen sich selbst in der Windows Registrierung registrieren. 
  
> [!NOTE]
> Administratoren und Benutzer können eine Gruppenrichtlinieneinstellung verwenden, um zu verhindern, dass Windows Desktopsuche Outlook Elemente indiziert. Weitere Informationen finden Sie unter [Erweitern Windows Desktopsuche.](https://msdn.microsoft.com/library/2eab146a-8516-4b95-b73c-ca7f980ba233%28Office.15%29.aspx) 
  
## <a name="registry-keys"></a>Registrierungsschlüssel

Auf einem Computer müssen alle Speicheranbieter, die indiziert werden sollen, nur unter einem der folgenden drei Registrierungsschlüssel in der Windows Registrierung registriert werden. Der MAPI-Protokollhandler sucht unter jedem dieser Schlüssel in der folgenden Reihenfolge:
  
1. [HKLM]\Software\Policies\Microsoft\Windows\Windows Search\
    
2. [HKLM]\Software\Microsoft\Windows\Windows Search\Preferences\
    
3. [HKCU]\Software\Microsoft\Windows\Windows Search\Preferences\
    
 Jeder Wert unter dem Schlüssel entspricht einem Speicheranbieter, der indiziert werden würde. Der Name des Werts ist die GUID (Globally Unique Identifier) des Speicheranbieters, der vom Typ **DWORD** ist und den Hexadezimalwert 0x00000001 hat. 
  
## <a name="guids-for-store-providers"></a>GUIDs für Store Anbieter

Die MAPI-Eigenschaft **[PR_MDB_PROVIDER](pidtagstoreprovider-canonical-property.md)** gibt die GUID eines MAPI-Speichers an. Die GUIDs für die Speicheranbieter, die Indizes Outlook, werden in der folgenden Tabelle beschrieben. 
  
||||
|:-----|:-----|:-----|
|**Typ des Store Anbieters** <br/> |**GUID** <br/> |**Hinweise** <br/> |
|Persönliche Ordnerdateien (. PST)  <br/> |{4154494E-BFF9-01B8-00AA-0037D96E0000}  <br/> |GUID wird in der öffentlichen Headerdatei mspst.h als **MSPST_UID_PROVIDER** <br/> |
|Exchange  <br/> |{C0A19454-7F29-1B10-A587-08002B2A2517}  <br/> |GUID ist in der öffentlichen Headerdatei "edkmdb.h" als **PbExchangeProviderPrimaryUserGuid** dokumentiert. <br/> |
|Öffentliche Ordner  <br/> |{70fab278-f7af-cd11-9bc8-00aa002fc45a}  <br/> |GUID ist in der öffentlichen Headerdatei "edkmdb.h" als **PbExchangeProviderPublicGuid** dokumentiert. <br/> |
|Outlook Connector für MSN  <br/> |{c34f5c97-eb05-bb4b-b199-2a7570ec7cf9}  <br/> |Keines  <br/> |
   
## <a name="see-also"></a>Siehe auch



[Informationen zur Speicher-API](about-the-store-api.md)

