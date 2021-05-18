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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 70932e703511235e9f5e32efd95b18d1b66494e2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316310"
---
# <a name="pidtagfolderwebviewinfo-cannonical-property"></a>PidTagFolderWebViewInfo (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält die URL für die Homepage eines Ordners in Microsoft Outlook. Diese Eigenschaft enthält einen binären Datenstrom namens **WebViewPersistenceObject**.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_FOLDER_WEBVIEWINFO  <br/> |
|Kennung:  <br/> |0x36DF  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |MAPI-Ordner  <br/> |
   
## <a name="remarks"></a>Hinweise

Eine Homepage-URL kann für jeden beliebigen Ordner Outlook werden. Auf diese Informationen kann in Outlook  der Registerkarte Startseite des Dialogfelds Eigenschaften für einen Ordner zugegriffen werden. 
  
Abhängig von bestimmten Richtlinieneinstellungen wird die Startseite möglicherweise von Outlook ignoriert, wenn der MAPI-Speicher, der diesen Ordner enthält, MSCAP_SECURE_FOLDER_HOMEPAGES in seiner [IMSCapabilities::GetCapabilities-Implementierung](pidtagfolderwebviewinfo-cannonical-property.md) nicht MSCAP_SECURE_FOLDER_HOMEPAGES berichtet. 
  
Sowohl der **Outlook als** auch ein öffentlicher Ordner können URLs für die Startseite enthalten. Der Ordner **Outlook Heute** verwendet jedoch einen anderen Mechanismus zum Verwalten der Startseiten-URL. dieser Mechanismus wird in diesem Thema nicht behandelt. In einem öffentlichen Ordner ist möglicherweise auch eine Homepage-URL definiert, die für einen Benutzer spezifisch ist. Diese Funktion wird in diesem Thema jedoch nicht beschrieben. 
  
Der Wert dieser Eigenschaft ist ein binärer Datenstrom namens **WebViewPersistenceObject**.
  
### <a name="webviewpersistenceobject-stream-structure"></a>WebViewPersistenceObject Stream Structure

Die **WebViewPersistenceObject-Streamstruktur** enthält Informationen zu einer Homepage-URL für einen Ordner. 
  
Datenelemente in dieser Struktur werden in der Bytereihenfolge little-endian gespeichert und folgen in der folgenden angegebenen Reihenfolge. 
  
> [!NOTE]
> In der folgenden Beschreibung werden möglicherweise nicht alle von der Datei unterstützten Feldwerte Outlook. Wenn Ihr Code daher einen vorhandenen Datenstrom liest, werden möglicherweise auch einige Flags gefunden, die hier nicht aufgeführt sind. Sie können diese Beschreibung jedoch verwenden, um programmgesteuert Werte für die **PidTagFolderWebViewInfo-Eigenschaft** zu erstellen, die Outlook versteht. 
  
 _dwVersion_
  
> DWORD (4 Byte). Die Version des Strukturformats. Ab Microsoft Office Outlook 2007 ist der einzige unterstützte Wert für dieses Feld wie folgt.
    
|**Wertname**|**Wert**|
|:-----|:-----|
|WEBVIEW_PERSISTENCE_VERSION  <br/> |0x00000002  <br/> |
   
 _dwType_
  
> DWORD (4 Byte). Der Typ der Startseiteninformationen. Ab Microsoft Office Outlook 2007 ist der einzige unterstützte Wert für dieses Feld wie folgt.
    
|**Wertname**|**Wert**|
|:-----|:-----|
|WEBVIEWURL  <br/> |0x00000001  <br/> |
   
 _dwFlags_
  
> DWORD (4 Byte). Eine Kombination aus Null oder mehr Flags, deren Werte und Bedeutungen in der folgenden Tabelle aufgeführt sind.
    
|Kennzeichenname****|****Value****|****Beschreibung****|
|:-----|:-----|:-----|
|WEBVIEW_FLAGS_SHOWBYDEFAULT  <br/> |0x00000001  <br/> |Das **Kontrollkästchen Homepage für** diesen Ordner standardmäßig  anzeigen wurde auf der Registerkarte Startseite des Dialogfelds Eigenschaften für einen Ordner aktiviert.  <br/> |
   
 _dwUnused[7]_
  
> Ein Array von 7 DWORD-Elementen (insgesamt 28 Byte). Nicht verwendet.
    
cbData
  
> Ein ULONG (4 Byte). Die Größe des  _wzURL-Datenelements_ in Bytes. 
    
 _wzURL_
  
> Ein Array von WCHAR-Elementen. Die UTF-16-Darstellung der URL-Zeichenfolge mit 0-gekündigter Startseite.
    
### <a name="webviewpersistenceobject-stream-sample"></a>WebViewPersistenceObject-Streambeispiel

In diesem Abschnitt wird ein Beispiel für einen **WebViewPersistenceObject-Stream** beschrieben. Der Datenstrom gibt die Homepage-URL " " https://www.microsoft.com an. 
  
 **Datenabbild**
  
Es folgt ein Datenabbild des Datenstroms, wie er in einem binären Editor angezeigt würde.
  
|**Stream offset**|**Datenbytes**|**ASCII-Daten**|
|:-----|:-----|:-----|
|0000000000  <br/> | `02 00 00 00 01 00 00 00 01 00 00 00 00 00 00 00` <br/> | `?...?...?.......` <br/> |
|0000000010  <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
|0000000020  <br/> | `00 00 00 00 00 00 00 00 32 00 00 00 68 00 74 00` <br/> | `........2...h.t.` <br/> |
|0000000030  <br/> | `74 00 70 00 3A 00 2F 00 2F 00 77 00 77 00 77 00` <br/> | `t.p.:././.w.w.w.` <br/> |
|0000000040  <br/> | `2E 00 6D 00 69 00 63 00 72 00 6F 00 73 00 6F 00` <br/> | `..m.i.c.r.o.s.o.` <br/> |
|0000000050  <br/> | `66 00 74 00 2E 00 63 00 6F 00 6D 00 00 00` <br/> | `f.t...c.o.m...` <br/> |
   
Im Folgenden finden Sie eine Analyse der Beispieldaten für den **WebViewPersistenceObject-Stream.** 
  
 _dwVersion_
  
> Offset 0x0, 4 Byte: 0x00000002 (WEBVIEW_PERSISTENCE_VERSION).
    
 _dwType_
  
> Offset 0x4, 4 Bytes: 0x00000001 (WEBVIEWURL).
    
 _dwFlags_
  
> Offset 0x8, 4 Byte: 0x00000001 (WEBVIEW_FLAGS_SHOWBYDEFAULT).
    
 _dwUnused[7]_
  
> Offset 0xC, 28 Byte: alle Nullen.
    
 _cbData_
  
> Offset 0x28, 4 Byte: 0x00000032.
    
 _wzURL_
  
> Offset 0x2C, 0x32 Bytes: Array von 25 WCHARs. Ein Unicode-Wert mit Nullendzeichenfolge: " https://www.microsoft.com ".
    

