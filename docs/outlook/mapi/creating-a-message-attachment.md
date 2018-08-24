---
title: Erstellen von e-Mail-Anlagen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 711b6765-7763-41ae-9ff8-61ca6ddd459d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 34d8dbeaf101d5ebb687403a2200bd0ad73b9998
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577100"
---
# <a name="creating-a-message-attachment"></a>Erstellen von e-Mail-Anlagen
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
E-Mail-Anlagen ist einige zusätzlichen Daten enthält, wie eine Datei, eine andere Nachricht oder ein OLE-Objekt, die zusammen mit einer Nachricht speichern oder senden können. Jede Anlage ist eine Auflistung von Eigenschaften, die diese identifiziert und beschreibt dieses Typs und wie es gerendert wird. Wie Empfänger können e-Mail-Anlagen nur über die Nachricht zugegriffen werden, die sie angehören. Aus diesem Grund muss für die Anlage verwendet werden, dessen Nachricht geöffnet sein.
  
## <a name="create-a-message-attachment"></a>Erstellen von e-Mail-Anlagen
  
1. Rufen Sie die Nachricht [IMessage::CreateAttach](imessage-createattach.md) -Methode, und übergeben Sie NULL als Schnittstellenbezeichner. **CreateAttach** gibt eine Zahl, die die neue Anlage in der Nachricht eindeutig identifiziert. Die Anzahl der Anlage wird in der Eigenschaft **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) gespeichert und gilt nur, solange die Nachricht mit Anlage geöffnet ist.
    
2. Rufen Sie [IMAPIProp::SetProps](imapiprop-setprops.md) , um **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)), um anzugeben, wie Sie Zugriff auf die Anlage festzulegen. **PR_ATTACH_METHOD** ist erforderlich. Legen Sie es auf: 
    
   - ATTACH_BY_VALUE, wenn die Anlage Binärdaten ist.
    
   - ATTACH_BY_REFERENCE, ATTACH_BY_REF_RESOLVE oder ATTACH_BY_REF_ONLY, wenn die Anlage eine Datei ist.
    
   - ATTACH_EMBEDDED_MSG, wenn die Anlage einer Nachricht ist.
    
   - ATTACH_OLE, wenn die Anlage ein OLE-Objekt ist.
    
3. Legen Sie die entsprechende Anlage Data-Eigenschaft:
    
   - **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) für binäre Daten und OLE-1-Objekte.
    
   - **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) für Dateien.
    
   - **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) für Nachrichten und OLE-2-Objekte.
    
4. Legen Sie **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)), die die Grafik Darstellung der Anlage für Datei oder binäre Anlagen enthalten soll. Legen Sie sie nicht für OLE-Objekte, die intern die Renderinginformationen gespeichert werden sollen, oder für angefügte Nachrichten. 
    
5. Legen Sie **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)), um anzugeben, wo die Anlage angezeigt werden soll. **PR_RENDERING_POSITION** gilt nur für Clients, die die **PR_BODY** -Eigenschaft festgelegt. Wenn Sie nur **PR_RTF_COMPRESSED**unterstützen, platzieren Sie die folgenden für Platzhalterinformationen in den komprimierten Stream:
    
   `\objattph`

   Wenn **PR_RENDERING_POSITION**festlegen möchten, weisen Sie entweder eine Zahl, die einen Ordnungszahlen Offset in Zeichen, mit dem ersten Zeichen des **PR_BODY** 0 ist, wird, wenn Sie müssen in der Nachricht Where kennen, die die Anlage gerendert wird, oder 0xFFFFFFFF, darstellt, wenn Sie nicht Anlagen in **PR_BODY**zu rendern.
    
6. Legen Sie **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)), um den kurzen Namen der Datei für eine Dateianlage anzugeben und **PR\_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)), um den Namen der Datei anzugeben, wie unterstützt auf einer Plattform, die das Format langer Dateiname behandelt. Beide Eigenschaften sind optional. Jedoch, wenn Sie **PR_ATTACH_LONG_FILENAME**festgelegt wird, legen Sie auch **PR_ATTACH_FILENAME**. 
    
7. Legen Sie **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), um den Namen für die Anlage anzugeben, die in einem Dialogfeld angezeigt werden können. PR_DISPLAY_NAME ist optional. 
    
## <a name="set-prattachdatabin"></a>PR_ATTACH_DATA_BIN festlegen
  
1. Rufen Sie [IMAPIProp::OpenProperty](imapiprop-openproperty.md) , um die Eigenschaft mit der **IStream** -Schnittstelle zu öffnen. 
    
2. Rufen Sie Wenn eine Datei die Daten enthält, und es geöffnet wird, oder wenn Sie explizite Kontrolle über Puffergröße benötigen, **IStream::Write** in einer Schleife, um die Daten im Stream-Objekt zu platzieren. 
    
3. Eine weitere Option besteht Aufrufen **OpenStreamOnFile nicht ausgeführt werden** , um Zugriff auf die Datendatei, und rufen Sie dann diesen Datenstrom **:: CopyTo** -Methode, um die Daten in das Stream-Objekt zurückgegebene **OpenProperty**Kopieren eines Stream-Objekts zu erstellen.
    
4. Der neue Stream **IStream:: Commit** -Methode aufrufen. 
    
## <a name="set-prattachdataobj"></a>PR_ATTACH_DATA_OBJ festlegen
  
1. Rufen Sie **IMAPIProp::OpenProperty** zum Öffnen die-Eigenschaft mit der **IStreamDocfile** -Schnittstelle ein Stream-Objekt zu erstellen, die mit strukturierten Speicher funktioniert. **IStreamDocfile** ist Zeichenfolgeneigenschaften Nachricht Clients geben eine höhere Leistung Möglichkeit zum Speichern und Abrufen von strukturierten Speicher implementiert. Die **IStreamDocfile** -Schnittstelle ist identisch mit **IStream**, jedoch ist sichergestellt, dass des Inhalts des Datenstroms wird als strukturierter Speicher formatiert werden. Wenn dieser Aufruf erfolgreich ist, erstellen Sie den Stream mit die gleichen Schritte zum Festlegen von **PR_ATTACH_DATA_BIN**.
    
2. Wenn **OpenProperty** ein Fehler auftritt: 
    
   1. Rufen Sie **OpenProperty** erneut für **IStorage**aufgefordert werden. 
      
   2. Rufen Sie **StgOpenStorage** , um das OLE-Objekt zu öffnen und ein Speicherobjekt zurückzugeben. 
      
   3. Rufen Sie das zurückgegebene Speicherobjekt **IStorage::CopyTo** -Methode zum Kopieren von auf das Speicherobjekt von **OpenProperty**zurückgegeben.
      
   4. Rufen Sie das neue Speicherobjekt **IStorage::Commit** -Methode. 
    
## <a name="set-prattachpathname"></a>PR_ATTACH_PATHNAME festlegen
  
1. Reservieren Sie eine [SPropValue](spropvalue.md) -Struktur, Festlegen des Members **UlPropTag** **PR_ATTACH_PATHNAME** und dem **Value.LPSZ** Mitglied in der Zeichenfolge, die den Dateinamen darstellt. 
    
2. Rufen Sie die Anlage [IMAPIProp::SetProps](imapiprop-setprops.md) -Methode. 
    
> [!NOTE]
> Wenn Ihre Plattform lange Dateinamen unterstützt, legen Sie **PR_ATTACH_PATHNAME** und **PR_ATTACH_LONG_PATHNAME**. Möglicherweise müssen, stellen Sie ein Betriebssystem aufrufen Kurzname abgerufen werden. 
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Anlagen](mapi-attachments.md)

