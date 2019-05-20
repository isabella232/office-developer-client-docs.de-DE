---
title: Informationen zum Registrieren von Speichern für die Indizierung
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: dd2aa06a-96e8-1291-18b5-fc3c40b74e4d
description: 'Letzte Änderung: 9. März 2015'
ms.openlocfilehash: 96322d12b3b7b334b5f78f81910dcf34c3fc78e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321826"
---
# <a name="about-registering-stores-for-indexing"></a>Informationen zum Registrieren von Speichern für die Indizierung

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Dieses Thema gilt speziell für die Sofortsuche in Microsoft Office Outlook 2007.
  
Mit der Sofortsuche können Sie Elemente in Outlook schnell auffinden. Sie verwendet Komponenten der Windows-Desktopsuche.
  
Der MAPI-Protokollhandler überprüft die Windows-Registrierung auf Speicher, die für Suchzwecke indizieren werden sollen. Speicheranbieter, die indiziert werden wollen, müssen in der Windows-Registrierung registriert werden.
  
Das Windows-Desktopsuche fügt standardmäßig die folgenden vier Arten von Speicheranbietern zur Windows-Registrierung hinzu, um die Indizierung zu ermöglichen:
  
- Speicher für persönliche Ordner-Dateien (PST)
    
-  Microsoft Exchange-Speicher, einschließlich aller Offlineordnerdateien (OST). 
    
-  Speicher für öffentliche Ordner. 
    
-  Speicher für Microsoft Office Outlook Connector für MSN. 
    
 Externe Speicheranbieter, die indiziert werden wollen, müssen sich in der Windows-Registrierung registrieren. 
  
> [!NOTE]
> Administratoren und Benutzer können eine Gruppenrichtlinieneinstellung verwenden, um zu verhindern, dass die Windows-Desktopsuche Outlook-Elemente indiziert. Weitere Informationen finden Sie unter [Erweitern der Windows-Desktopsuche](https://msdn.microsoft.com/library/2eab146a-8516-4b95-b73c-ca7f980ba233%28Office.15%29.aspx). 
  
## <a name="registry-keys"></a>Registrierungsschlüssel

Auf einem Computer müssen alle Speicheranbieter, die indiziert werden wollen, unter nur einem der folgenden drei Registrierungsschlüssel in der Windows-Registrierung registriert werden. Der MAPI-Protokollhandler sucht unter jedem dieser Schlüssel in der folgenden Reihenfolge:
  
1. [HKLM]\Software\Policies\Microsoft\Windows\Windows Search\
    
2. [HKLM]\Software\Microsoft\Windows\Windows Search\Preferences\
    
3. [HKCU]\Software\Microsoft\Windows\Windows Search\Preferences\
    
 Jeder Wert unter dem Schlüssel entspricht einem Speicheranbieter, der indiziert werden soll. Der Name des Werts ist der Globally Unique Identifier (GUID) des Speicheranbieters, der vom Typ **DWORD** ist und den hexadezimalen Wert 0x00000001 aufweist. 
  
## <a name="guids-for-store-providers"></a>GUIDs für Speicheranbieter

Die MAPI-Eigenschaft **[PR_MDB_PROVIDER](pidtagstoreprovider-canonical-property.md)** gibt die GUID eines MAPI-Speichers an. Die GUIDs für die Speicheranbieter, die Outlook indiziert, sind in der folgenden Tabelle beschrieben. 
  
||||
|:-----|:-----|:-----|
|**Typ des Speicheranbieters** <br/> |**GUID** <br/> |**Hinweise** <br/> |
|Persönliche Ordner-Dateien (PST)  <br/> |{4154494E-BFF9-01B8-00AA-0037D96E0000}  <br/> |Die GUID wird in der öffentlichen Headerdatei "mspst.h" als **MSPST_UID_PROVIDER** dokumentiert. <br/> |
|Exchange  <br/> |{C0A19454-7F29-1B10-A587-08002B2A2517}  <br/> |Die GUID wird in der öffentlichen Headerdatei "edkmdb.h" als **pbExchangeProviderPrimaryUserGuid** dokumentiert. <br/> |
|Öffentliche Ordner  <br/> |{70fab278-f7af-cd11-9bc8-00aa002fc45a}  <br/> |Die GUID wird in der öffentlichen Headerdatei "edkmdb.h" als **pbExchangeProviderPublicGuid** dokumentiert. <br/> |
|Outlook-Connector für MSN  <br/> |{c34f5c97-eb05-bb4b-b199-2a7570ec7cf9}  <br/> |Keine  <br/> |
   
## <a name="see-also"></a>Siehe auch



[Informationen zur Speicher-API](about-the-store-api.md)

