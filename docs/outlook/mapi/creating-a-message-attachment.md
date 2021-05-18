---
title: Erstellen einer Nachrichtenanlage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 711b6765-7763-41ae-9ff8-61ca6ddd459d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2bdba3574c962c825f45cd098efa1cba6e21a4ea
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405996"
---
# <a name="creating-a-message-attachment"></a>Erstellen einer Nachrichtenanlage
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bei einer Nachrichtenanlage handelt es sich um einige zusätzliche Daten, z. B. eine Datei, eine andere Nachricht oder ein OLE-Objekt, die Sie zusammen mit einer Nachricht senden oder speichern können. Jede Anlage verfügt über eine Auflistung von Eigenschaften, die sie identifiziert und den Typ und die Art des Renderns beschreibt. Wie Empfänger können Nachrichtenanlagen nur über die Nachricht zugegriffen werden, zu der sie gehören. Damit eine Anlage verwendet werden kann, muss ihre Nachricht daher geöffnet sein.
  
## <a name="create-a-message-attachment"></a>Erstellen einer Nachrichtenanlage
  
1. Rufen Sie die [IMessage::CreateAttach-Methode](imessage-createattach.md) der Nachricht auf, und übergeben Sie NULL als Schnittstellenbezeichner. **CreateAttach** gibt eine Zahl zurück, die die neue Anlage innerhalb der Nachricht eindeutig identifiziert. Die Anlagennummer wird in der **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) -Eigenschaft gespeichert und ist nur gültig, solange die Nachricht mit der Anlage geöffnet ist.
    
2. Rufen [Sie IMAPIProp::SetProps](imapiprop-setprops.md) auf, um **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) zu legen, um anzugeben, wie auf die Anlage zugegriffen werden soll. **PR_ATTACH_METHOD** erforderlich. Legen Sie es auf: 
    
   - ATTACH_BY_VALUE, wenn es sich bei der Anlage um Binärdaten handelt.
    
   - ATTACH_BY_REFERENCE, ATTACH_BY_REF_RESOLVE oder ATTACH_BY_REF_ONLY, wenn es sich bei der Anlage um eine Datei handelt.
    
   - ATTACH_EMBEDDED_MSG, wenn es sich bei der Anlage um eine Nachricht handelt.
    
   - ATTACH_OLE, wenn es sich bei der Anlage um ein OLE-Objekt handelt.
    
3. Legen Sie die entsprechende Anlagedateneigenschaft auf:
    
   - **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) für Binärdaten und OLE 1-Objekte.
    
   - **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) für Dateien.
    
   - **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) für Nachrichten und OLE 2-Objekte.
    
4. Legen **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) fest, um die grafische Darstellung der Anlage für Datei- oder binäre Anlagen zu speichern. Legen Sie sie nicht für OLE-Objekte fest, die die Renderinginformationen intern speichern, oder für angefügte Nachrichten. 
    
5. Legen **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) fest, um anzugeben, wo die Anlage angezeigt werden soll. **PR_RENDERING_POSITION** gilt nur für Clients, die die PR_BODY **festlegen.** Wenn Sie nur **PR_RTF_COMPRESSED** unterstützen, platzieren Sie die folgenden Platzhalterinformationen im komprimierten Datenstrom:
    
   `\objattph`

   Weisen Sie zum Festlegen von **PR_RENDERING_POSITION** entweder eine Zahl zu, die einen Ordnungsversatz in Zeichen darstellt, wobei das erste Zeichen von **PR_BODY** 0 ist, wenn Sie wissen müssen, wo in der Nachricht die Anlage gerendert wird, oder 0xFFFFFFFF, wenn Sie Anlagen nicht innerhalb von **PR_BODY rendern.**
    
6. Legen Sie **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) fest, um den kurzen Namen der Datei für eine Dateianlage und **PR \_ ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) anzugeben, um den Namen der Datei anzugeben, der auf einer Plattform unterstützt wird, die das lange Dateinamenformat verarbeitet. Beide Eigenschaften sind optional. Wenn Sie jedoch **PR_ATTACH_LONG_FILENAME** festlegen, legen Sie auch **PR_ATTACH_FILENAME.** 
    
7. Legen **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) fest, um den Namen der Anlage anzugeben, die in einem Dialogfeld angezeigt werden kann. PR_DISPLAY_NAME ist optional. 
    
## <a name="set-pr_attach_data_bin"></a>Festlegen PR_ATTACH_DATA_BIN
  
1. Rufen [Sie IMAPIProp::OpenProperty auf,](imapiprop-openproperty.md) um die Eigenschaft mit der **IStream-Schnittstelle zu** öffnen. 
    
2. Wenn eine Datei die Daten enthält und geöffnet ist oder Wenn Sie explizite Kontrolle über die Puffergröße benötigen, rufen Sie **IStream::Write** in einer Schleife auf, um die Daten in den Datenstrom zu platzieren. 
    
3. Eine weitere Option ist das Aufrufen von **OpenStreamOnFile** zum Erstellen eines Datenstroms für den Zugriff auf die Datendatei und anschließendes Aufrufen der **IStream::CopyTo-Methode** dieses Datenstroms, um die Daten in den von **OpenProperty** zurückgegebenen Datenstrom zu kopieren.
    
4. Rufen Sie die **IStream::Commit-Methode des neuen Datenstroms** auf. 
    
## <a name="set-pr_attach_data_obj"></a>Festlegen PR_ATTACH_DATA_OBJ
  
1. Rufen **Sie IMAPIProp::OpenProperty auf,** um die Eigenschaft mit der **IStreamDocfile-Schnittstelle** zu öffnen, um einen Datenstrom zu erstellen, der mit strukturiertem Speicher funktioniert. **IStreamDocfile** wird von Nachrichtenspeicheranbietern implementiert, um Clients eine bessere Leistung zum Speichern und Abrufen von strukturiertem Speicher zu bieten. Die **IStreamDocfile-Schnittstelle** ist mit **IStream** identisch, aber der Inhalt des Datenstroms wird garantiert als strukturierter Speicher formatiert. Wenn dieser Aufruf erfolgreich ist, erstellen Sie den Datenstrom mit den gleichen Schritten, die für das Festlegen von **PR_ATTACH_DATA_BIN.**
    
2. Wenn **OpenProperty fehlschlägt:** 
    
   1. Rufen **Sie OpenProperty** erneut auf, und fordern **Sie IStorage an.** 
      
   2. Rufen **Sie StgOpenStorage auf,** um das OLE-Objekt zu öffnen und ein Speicherobjekt zurückzukehren. 
      
   3. Rufen Sie die **IStorage::CopyTo-Methode** des zurückgegebenen Speicherobjekts auf, um in das von OpenProperty zurückgegebene **Speicherobjekt zu kopieren.**
      
   4. Rufen Sie die **IStorage::Commit-Methode** des neuen Speicherobjekts auf. 
    
## <a name="set-pr_attach_pathname"></a>Festlegen PR_ATTACH_PATHNAME
  
1. Weisen Sie [eine SPropValue-Struktur](spropvalue.md) zu, und setzen Sie das **element ulPropTag** auf **PR_ATTACH_PATHNAME** und das **Value.LPSZ-Element** auf die Zeichenzeichenfolge, die den Dateinamen darstellt. 
    
2. Rufen Sie die [IMAPIProp::SetProps-Methode der Anlage](imapiprop-setprops.md) auf. 
    
> [!NOTE]
> Wenn Ihre Plattform lange Dateinamen unterstützt, legen Sie sowohl PR_ATTACH_PATHNAME **als** auch **PR_ATTACH_LONG_PATHNAME.** Möglicherweise muss ein Betriebssystemaufruf ausgeführt werden, um den kurzen Dateinamen abzurufen. 
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Anlagen](mapi-attachments.md)

