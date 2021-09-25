---
title: PidTagFolderWebViewInfo (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagFolderWebViewInfo
api_type:
- HeaderDef
ms.assetid: 96ea23df-aa4f-4b3e-9663-e7db39f668c1
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 28faabf8655edcc6c1670191641287ab249843e2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59563560"
---
# <a name="pidtagfolderwebviewinfo-cannonical-property"></a>PidTagFolderWebViewInfo (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält die URL für die Startseite eines Ordners in Microsoft Outlook. Diese Eigenschaft enthält einen binären Datenstrom namens **WebViewPersistenceObject**.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_FOLDER_WEBVIEWINFO  <br/> |
|Kennung:  <br/> |0x36DF  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |MAPI-Ordner  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Eine Homepage-URL kann für jeden Outlook Ordner angegeben werden. Auf diese Informationen kann in Outlook über die Registerkarte **"Startseite"** des Dialogfelds "Eigenschaften" für einen Ordner zugegriffen werden. 
  
Abhängig von bestimmten Richtlinieneinstellungen wird die Startseite möglicherweise von Outlook ignoriert, wenn der MAPI-Speicher, der diesen Ordner enthält, keine MSCAP_SECURE_FOLDER_HOMEPAGES in der [IMSCapabilities::GetCapabilities-Implementierung](pidtagfolderwebviewinfo-cannonical-property.md) meldet. 
  
Sowohl der **Ordner "Outlook Heute"** als auch ein öffentlicher Ordner können UrLs der Startseite aufweisen. Der Ordner **"Outlook Heute"** verwendet jedoch einen anderen Mechanismus zum Verwalten seiner Homepage-URL. Dieser Mechanismus wird in diesem Thema nicht behandelt. Für einen öffentlichen Ordner ist möglicherweise auch eine startseiten-URL definiert, die für einen Benutzer spezifisch ist. Diese Funktion wird in diesem Thema jedoch nicht beschrieben. 
  
Der Wert dieser Eigenschaft ist ein binärer Datenstrom namens **WebViewPersistenceObject**.
  
### <a name="webviewpersistenceobject-stream-structure"></a>WebViewPersistenceObject-Datenstromstruktur

Die **WebViewPersistenceObject-Datenstromstruktur** enthält Informationen zu einer Homepage-URL für einen Ordner. 
  
Datenelemente in dieser Struktur werden in kleiner endischer Bytereihenfolge gespeichert, unmittelbar nacheinander in der folgenden angegebenen Reihenfolge. 
  
> [!NOTE]
> Die folgende Beschreibung listet möglicherweise nicht alle Feldwerte auf, die von Outlook unterstützt werden. Wenn Ihr Code daher einen vorhandenen Datenstrom liest, werden möglicherweise auch einige Flags gefunden, die hier nicht aufgeführt sind. Sie können diese Beschreibung jedoch verwenden, um programmgesteuert Werte für die **PidTagFolderWebViewInfo-Eigenschaft** zu erstellen, die Outlook verstehen. 
  
 _konstanteVersion_
  
> DWORD (4 Bytes). Die Version des Formats der Struktur. Ab Microsoft Office Outlook 2007 wird der einzige unterstützte Wert für dieses Feld wie folgt unterstützt.
    
|**Wertname**|**Wert**|
|:-----|:-----|
|WEBVIEW_PERSISTENCE_VERSION  <br/> |0x00000002  <br/> |
   
 _für "wettertype"_
  
> DWORD (4 Bytes). Der Typ der Homepageinformationen. Ab Microsoft Office Outlook 2007 wird der einzige unterstützte Wert für dieses Feld wie folgt unterstützt.
    
|**Wertname**|**Wert**|
|:-----|:-----|
|WEBVIEWURL  <br/> |0x00000001  <br/> |
   
 _Dwflags_
  
> DWORD (4 Bytes). Eine Kombination aus null oder mehr Flags, deren Werte und Bedeutungen in der folgenden Tabelle aufgeführt sind.
    
|Flagname|****Value****|****Beschreibung****|
|:-----|:-----|:-----|
|WEBVIEW_FLAGS_SHOWBYDEFAULT  <br/> |0x00000001  <br/> |Das **Kontrollkästchen "Startseite standardmäßig anzeigen" für diesen Ordner** wurde auf der Registerkarte **"Homepage"** des Dialogfelds "Eigenschaften" für einen Ordner aktiviert.  <br/> |
   
 _wetterUnused[7]_
  
> Ein Array von 7 DWORD-Elementen (insgesamt 28 Bytes). Unbenutzte.
    
Cbdata
  
> Ein ULONG (4 Bytes). Die Größe des  _wzURL-Datenelements_ in Bytes. 
    
 _wzURL_
  
> Ein Array von WCHAR-Elementen. Die UTF-16-Darstellung der URL-Zeichenfolge der Null-Endseite.
    
### <a name="webviewpersistenceobject-stream-sample"></a>WebViewPersistenceObject-Streambeispiel

In diesem Abschnitt wird ein Beispiel für einen **WebViewPersistenceObject-Stream** beschrieben. Der Stream gibt die Startseiten-URL " https://www.microsoft.com " an. 
  
 **Datenabbild**
  
Es folgt ein Datenabbild des Datenstroms, wie es in einem binären Editor angezeigt wird.
  
|**Datenstromversatz**|**Datenbytes**|**ASCII-Daten**|
|:-----|:-----|:-----|
|0000000000  <br/> | `02 00 00 00 01 00 00 00 01 00 00 00 00 00 00 00` <br/> | `?...?...?.......` <br/> |
|0000000010  <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
|0000000020  <br/> | `00 00 00 00 00 00 00 00 32 00 00 00 68 00 74 00` <br/> | `........2...h.t.` <br/> |
|0000000030  <br/> | `74 00 70 00 3A 00 2F 00 2F 00 77 00 77 00 77 00` <br/> | `t.p.:././.w.w.w.` <br/> |
|0000000040  <br/> | `2E 00 6D 00 69 00 63 00 72 00 6F 00 73 00 6F 00` <br/> | `..m.i.c.r.o.s.o.` <br/> |
|0000000050  <br/> | `66 00 74 00 2E 00 63 00 6F 00 6D 00 00 00` <br/> | `f.t...c.o.m...` <br/> |
   
Es folgt eine Analyse der Beispieldaten für den **WebViewPersistenceObject-Stream.** 
  
 _konstanteVersion_
  
> Offset 0x0, 4 Bytes: 0x00000002 (WEBVIEW_PERSISTENCE_VERSION).
    
 _für "wettertype"_
  
> Offset 0x4, 4 Bytes: 0x00000001 (WEBVIEWURL).
    
 _Dwflags_
  
> Offset 0x8, 4 Bytes: 0x00000001 (WEBVIEW_FLAGS_SHOWBYDEFAULT).
    
 _wetterUnused[7]_
  
> Offset 0xC, 28 Byte: alle Nullen.
    
 _Cbdata_
  
> Offset 0x28, 4 Bytes: 0x00000032.
    
 _wzURL_
  
> Offset 0x2C, 0x32 Bytes: Array von 25 WCHARs. Ein unicode nullbeendiger Zeichenfolgenwert: " https://www.microsoft.com ".
    

