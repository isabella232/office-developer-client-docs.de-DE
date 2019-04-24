---
title: PidTagFolderWebViewInfo (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFolderWebViewInfo
api_type:
- HeaderDef
ms.assetid: 96ea23df-aa4f-4b3e-9663-e7db39f668c1
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 70932e703511235e9f5e32efd95b18d1b66494e2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316310"
---
# <a name="pidtagfolderwebviewinfo-cannonical-property"></a>PidTagFolderWebViewInfo (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält die URL für die Startseite eines Ordners in Microsoft Outlook. Diese Eigenschaft enthält einen binären Datenstromnamens **WebViewPersistenceObject**.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_FOLDER_WEBVIEWINFO  <br/> |
|Kennung:  <br/> |0x36DF  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |MAPI-Ordner  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Für einen beliebigen Outlook-Ordner kann eine Homepage-URL angegeben werden. Auf diese Informationen kann in Outlook über die Registerkarte **Startseite** des Dialogfelds Eigenschaften für einen Ordner zugegriffen werden. 
  
Abhängig von bestimmten Richtlinieneinstellungen wird die Homepage möglicherweise von Outlook ignoriert, wenn der MAPI-Speicher, der diesen Ordner enthält, MSCAP_SECURE_FOLDER_HOMEPAGES nicht in seiner [IMSCapabilities:: getCapabilities](pidtagfolderwebviewinfo-cannonical-property.md) -Implementierung meldet. 
  
Sowohl der **Outlook Heute** -Ordner als auch ein öffentlicher Ordner können URLs der Homepage enthalten. Der **Outlook Heute** -Ordner verwendet jedoch einen anderen Mechanismus, um die URL der Startseite zu verwalten. Dieser Mechanismus wird in diesem Thema nicht behandelt. Ein öffentlicher Ordner kann auch eine für einen benutzerspezifische Homepage-URL enthalten. Diese Funktion wird jedoch in diesem Thema nicht beschrieben. 
  
Der Wert dieser Eigenschaft ist ein binärer Datenstromnamens **WebViewPersistenceObject**.
  
### <a name="webviewpersistenceobject-stream-structure"></a>WebViewPersistenceObject-Datenstrom Struktur

Die **WebViewPersistenceObject** -Datenstrom Struktur enthält Informationen zu einer Homepage-URL für einen Ordner. 
  
Datenelemente in dieser Struktur werden in der Little-Endian-Bytereihenfolge gespeichert, unmittelbar nach einander in der folgenden angegebenen Reihenfolge. 
  
> [!NOTE]
> In der folgenden Beschreibung werden möglicherweise nicht alle von Outlook unterstützten Feldwerte aufgeführt; Wenn Ihr Code also einen vorhandenen Stream liest, werden möglicherweise auch einige Flags gefunden, die hier nicht aufgeführt sind. Sie können diese Beschreibung jedoch zum programmgesteuerten Erstellen von Werten für die **PidTagFolderWebViewInfo** -Eigenschaft verwenden, die Outlook verstehen wird. 
  
 _dwVersion_
  
> DWORD (4 Bytes). Die Version des Formats der Struktur. Ab Microsoft Office Outlook 2007 ist der einzige unterstützte Wert für dieses Feld wie folgt.
    
|**Wertname**|**Wert**|
|:-----|:-----|
|WEBVIEW_PERSISTENCE_VERSION  <br/> |0x00000002  <br/> |
   
 _dwType_
  
> DWORD (4 Bytes). Der Typ der Homepage Informationen. Ab Microsoft Office Outlook 2007 ist der einzige unterstützte Wert für dieses Feld wie folgt.
    
|**Wertname**|**Wert**|
|:-----|:-----|
|WEBVIEWURL  <br/> |0x00000001  <br/> |
   
 _dwFlags_
  
> DWORD (4 Bytes). Eine Kombination aus null oder mehr Flags, deren Werte und Bedeutungen in der folgenden Tabelle aufgeführt sind.
    
|Kennzeichenname * * * *|****Value****|****Beschreibung****|
|:-----|:-----|:-----|
|WEBVIEW_FLAGS_SHOWBYDEFAULT  <br/> |0x00000001  <br/> |Das Kontrollkästchen **Homepage standardmäßig für diesen Ordner anzeigen** wurde auf der Registerkarte **Startseite** des Dialogfelds Eigenschaften für einen Ordner aktiviert.  <br/> |
   
 _dwUnused [7]_
  
> Ein Array von 7 DWORD-Elementen (insgesamt 28 Byte). Nicht verwendete.
    
cbData
  
> Ein ULONG (4 Bytes). Die Größe des _wzURL_ -Datenelements in Bytes. 
    
 _wzURL_
  
> Ein Array von Typ WCHAR-Elementen. Die UTF-16-Darstellung der nullterminierten URL-Zeichenfolge der Startseite.
    
### <a name="webviewpersistenceobject-stream-sample"></a>WebViewPersistenceObject-Stream-Beispiel

In diesem Abschnitt wird ein Beispiel für einen **WebViewPersistenceObject** -Stream beschrieben. Der Stream gibt die URLhttps://www.microsoft.comder Startseite an. 
  
 **Daten Dump**
  
Es folgt ein Daten Dump des Streams, wie er in einem binären Editor angezeigt würde.
  
|**Datenstrom Offset**|**Datenbytes**|**ASCII-Daten**|
|:-----|:-----|:-----|
|0000000000  <br/> | `02 00 00 00 01 00 00 00 01 00 00 00 00 00 00 00` <br/> | `?...?...?.......` <br/> |
|0000000010  <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
|0000000020  <br/> | `00 00 00 00 00 00 00 00 32 00 00 00 68 00 74 00` <br/> | `........2...h.t.` <br/> |
|0000000030  <br/> | `74 00 70 00 3A 00 2F 00 2F 00 77 00 77 00 77 00` <br/> | `t.p.:././.w.w.w.` <br/> |
|0000000040  <br/> | `2E 00 6D 00 69 00 63 00 72 00 6F 00 73 00 6F 00` <br/> | `..m.i.c.r.o.s.o.` <br/> |
|0000000050  <br/> | `66 00 74 00 2E 00 63 00 6F 00 6D 00 00 00` <br/> | `f.t...c.o.m...` <br/> |
   
Es folgt eine Analyse der Beispieldaten für den **WebViewPersistenceObject** -Stream. 
  
 _dwVersion_
  
> Offset 0x0 festlegen bytes: 0x00000002 (WEBVIEW_PERSISTENCE_VERSION).
    
 _dwType_
  
> Offset 0x4 bytes: 0x00000001 (WEBVIEWURL).
    
 _dwFlags_
  
> Offset 0x8 bytes: 0x00000001 (WEBVIEW_FLAGS_SHOWBYDEFAULT).
    
 _dwUnused [7]_
  
> Offset 0xC, 28 Byte: alle Nullen.
    
 _cbData_
  
> Offset 0x28 bytes: 0x00000032.
    
 _wzURL_
  
> Offset 0X2c beansprucht, 0x32 bytes: Array von 25 WCHARs. Ein Unicode-Wert mit der Zeichenfolge 0https://www.microsoft.com(null): "".
    

