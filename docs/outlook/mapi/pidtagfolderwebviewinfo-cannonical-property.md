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
ms.openlocfilehash: eec8ea4b4ddee8b6c399bbb4871c286fea4fae3d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588405"
---
# <a name="pidtagfolderwebviewinfo-cannonical-property"></a>PidTagFolderWebViewInfo (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält die URL für die Homepage eines Ordners in Microsoft Outlook. Diese Eigenschaft enthält einen binären Datenstrom **WebViewPersistenceObject**aufgerufen.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_FOLDER_WEBVIEWINFO  <br/> |
|Kennung:  <br/> |0x36DF  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |MAPI-Ordner  <br/> |
   
## <a name="remarks"></a>Bemerkungen

URL der Startseite kann für alle Outlook-Ordner angegeben werden. Diese Informationen kann über die Registerkarte " **Homepage** " im Dialogfeld Eigenschaften für einen Ordner in Outlook zugegriffen werden. 
  
Je nach bestimmten Richtlinieneinstellungen möglicherweise auf der Startseite von Outlook ignoriert, wenn der MAPI-Informationsspeicher, der dieser Ordner enthält keine MSCAP_SECURE_FOLDER_HOMEPAGES in seiner Implementierung [IMSCapabilities::GetCapabilities](pidtagfolderwebviewinfo-cannonical-property.md) meldet. 
  
Den Ordner **Outlook Heute** und einem öffentlichen Ordner können Homepage-URLs haben. Der Ordner **Outlook Heute** verwendet jedoch einen anderen Mechanismus zum Verwalten von des URL der Startseite; Dieser Mechanismus ist nicht in diesem Thema behandelt. Ein öffentlicher Ordner möglicherweise auch eine Homepage-URL definiert, die für einen Benutzer ist. Diese Funktion wird jedoch nicht in diesem Thema beschrieben. 
  
Der Wert dieser Eigenschaft ist einen binären Datenstrom **WebViewPersistenceObject**aufgerufen.
  
### <a name="webviewpersistenceobject-stream-structure"></a>WebViewPersistenceObject Stream-Struktur

Die **WebViewPersistenceObject** Stream-Datenstruktur enthält Informationen über eine Homepage-URL für einen Ordner. 
  
Data-Elemente in dieser Struktur werden in little-Endian-Bytereihenfolge, unmittelbar auf voneinander in der angegebenen Reihenfolge gespeichert. 
  
> [!NOTE]
> In der folgenden Beschreibung möglicherweise nicht Auflisten aller die Feldwerte von Outlook unterstützt; aus diesem Grund, wenn der Code einen vorhandenen Stream liest, möglicherweise einige Flags, die hier nicht aufgeführt sind auch gefunden werden. Diese Beschreibung können Sie jedoch die um Werte für die **PidTagFolderWebViewInfo** -Eigenschaft programmgesteuert zu erstellen, die Outlook verstehen. 
  
 _dwVersion_
  
> Ein DWORD-Wert (4 Bytes). Die Version des Formats der Struktur. Ab Microsoft Office Outlook 2007 ist der einzige unterstützte Wert für dieses Feld wie folgt.
    
|**Wertname**|**Wert**|
|:-----|:-----|
|WEBVIEW_PERSISTENCE_VERSION  <br/> |0x00000002  <br/> |
   
 _dwType_
  
> Ein DWORD-Wert (4 Bytes). Der Typ der Informationen zur Homepage. Ab Microsoft Office Outlook 2007 ist der einzige unterstützte Wert für dieses Feld wie folgt.
    
|**Wertname**|**Wert**|
|:-----|:-----|
|WEBVIEWURL  <br/> |0x00000001  <br/> |
   
 _dwFlags_
  
> Ein DWORD-Wert (4 Bytes). Eine Kombination aus null oder mehr flags, deren Werte und Bedeutung sind in der folgenden Tabelle aufgeführt.
    
|Flag Namen ***|Wert ***|****Beschreibung****|
|:-----|:-----|:-----|
|WEBVIEW_FLAGS_SHOWBYDEFAULT  <br/> |0x00000001  <br/> |Aktivieren Sie das Kontrollkästchen **Homepage in der Standardeinstellung für diesen Ordner anzeigen** wurde in der Registerkarte **Startseite** im Dialogfeld Eigenschaften für einen Ordner überprüft.  <br/> |
   
 _DwUnused [7]_
  
> Ein Array von 7 DWORD-Elemente (insgesamt 28 Bytes). Nicht verwendet.
    
cbData
  
> Ein ULONG (4 Bytes). Die Größe des _WzURL_ -Data-Element in Bytes. 
    
 _wzURL_
  
> Ein Array von WCHAR Elemente. Die UTF-16-Darstellung der URL Homepage NULL endende Zeichenfolge.
    
### <a name="webviewpersistenceobject-stream-sample"></a>WebViewPersistenceObject Stream-Beispiel

Dieser Abschnitt beschreibt ein Beispiel eines **WebViewPersistenceObject** Stream-Objekts. Das Stream-Objekt gibt die URL der Startseite "http://www.microsoft.com". 
  
 **Daten dump**
  
Im folgenden finden ein Abbild der Daten des Stream-Objekts, wie er in einem binären-Editor angezeigt.
  
|**Stream-offset**|**Datenbytes**|**ASCII-Daten**|
|:-----|:-----|:-----|
|0000000000  <br/> | `02 00 00 00 01 00 00 00 01 00 00 00 00 00 00 00` <br/> | `?...?...?.......` <br/> |
|0000000010  <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
|0000000020  <br/> | `00 00 00 00 00 00 00 00 32 00 00 00 68 00 74 00` <br/> | `........2...h.t.` <br/> |
|0000000030  <br/> | `74 00 70 00 3A 00 2F 00 2F 00 77 00 77 00 77 00` <br/> | `t.p.:././.w.w.w.` <br/> |
|0000000040  <br/> | `2E 00 6D 00 69 00 63 00 72 00 6F 00 73 00 6F 00` <br/> | `..m.i.c.r.o.s.o.` <br/> |
|0000000050  <br/> | `66 00 74 00 2E 00 63 00 6F 00 6D 00 00 00` <br/> | `f.t...c.o.m...` <br/> |
   
Es folgt eine Analyse der Beispieldaten für den **WebViewPersistenceObject** -Stream. 
  
 _dwVersion_
  
> Offset 0 x 0, 4 Bytes: 0 x 00000002 (WEBVIEW_PERSISTENCE_VERSION).
    
 _dwType_
  
> Offset 0, 4 Bytes x 4: 0 x 00000001 (WEBVIEWURL).
    
 _dwFlags_
  
> Offset 0 x 8, 4 Bytes: 0 x 00000001 (WEBVIEW_FLAGS_SHOWBYDEFAULT).
    
 _DwUnused [7]_
  
> Offset 0xC 28 Bytes: Nullen.
    
 _cbData_
  
> Offset 0, 4 Bytes x 28: 0x00000032.
    
 _wzURL_
  
> Offset 0x2C, 0 x 32 Bytes: Array von 25 WCHARs so lang wie. Unicode-Wert NULL endende Zeichenfolge: "http://www.microsoft.com".
    

