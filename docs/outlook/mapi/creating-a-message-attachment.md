---
title: Erstellen einer Nachrichtenanlage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 711b6765-7763-41ae-9ff8-61ca6ddd459d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e9d0d0c26dd04593aacba9db61cc85cda0a8aac9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592669"
---
# <a name="creating-a-message-attachment"></a>Erstellen einer Nachrichtenanlage
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bei einer Nachrichtenanlage handelt es sich um einige zusätzliche Daten, z. B. eine Datei, eine andere Nachricht oder ein OLE-Objekt, die Sie zusammen mit einer Nachricht senden oder speichern können. Jede Anlage verfügt über eine Auflistung von Eigenschaften, die sie identifiziert und deren Typ und darstellungsweise beschreibt. Wie Empfänger kann nur über die Nachricht, zu der sie gehören, auf Nachrichtenanlagen zugegriffen werden. Daher muss die Nachricht geöffnet sein, damit eine Anlage verwendet werden kann.
  
## <a name="create-a-message-attachment"></a>Erstellen einer Nachrichtenanlage
  
1. Rufen Sie die [IMessage::CreateAttach-Methode](imessage-createattach.md) der Nachricht auf, und übergeben Sie NULL als Schnittstellenbezeichner. **CreateAttach** gibt eine Zahl zurück, die die neue Anlage innerhalb der Nachricht eindeutig identifiziert. Die Anlagennummer wird in der **eigenschaft PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) gespeichert und ist nur gültig, solange die Nachricht, die die Anlage enthält, geöffnet ist.
    
2. Rufen Sie [IMAPIProp::SetProps](imapiprop-setprops.md) auf, um **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) festzulegen, um anzugeben, wie auf die Anlage zugegriffen werden soll. **PR_ATTACH_METHOD** ist erforderlich. Legen Sie folgendes fest: 
    
   - ATTACH_BY_VALUE, wenn es sich bei der Anlage um binäre Daten handelt.
    
   - ATTACH_BY_REFERENCE, ATTACH_BY_REF_RESOLVE oder ATTACH_BY_REF_ONLY, wenn die Anlage eine Datei ist.
    
   - ATTACH_EMBEDDED_MSG, ob es sich bei der Anlage um eine Nachricht handelt.
    
   - ATTACH_OLE, wenn es sich bei der Anlage um ein OLE-Objekt handelt.
    
3. Legen Sie die entsprechende Anlagendateneigenschaft fest:
    
   - **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) für Binärdaten und OLE 1-Objekte.
    
   - **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) für Dateien.
    
   - **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) für Nachrichten und OLE 2-Objekte.
    
4. Legen Sie **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) fest, um die grafische Darstellung der Anlage für Datei- oder binäre Anlagen zu speichern. Legen Sie es nicht für OLE-Objekte fest, die die Renderinginformationen intern speichern, oder für angefügte Nachrichten. 
    
5. Legen Sie **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) fest, um anzugeben, wo die Anlage angezeigt werden soll. **PR_RENDERING_POSITION** gilt nur für Clients, die die **PR_BODY-Eigenschaft** festlegen. Wenn Sie nur **PR_RTF_COMPRESSED** unterstützen, platzieren Sie die folgenden Platzhalterinformationen im komprimierten Datenstrom:
    
   `\objattph`

   Um **PR_RENDERING_POSITION** festzulegen, weisen Sie entweder eine Zahl zu, die einen Ordnungsversatz in Zeichen darstellt, wobei das erste Zeichen von **PR_BODY** 0 ist, wenn Sie wissen müssen, wo in der Nachricht die Anlage gerendert wird, oder 0xFFFFFFFF, wenn Sie Anlagen nicht innerhalb **PR_BODY** rendern.
    
6. Legen Sie **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) fest, um den Kurznamen der Datei für eine Dateianlage anzugeben, und **\_ PR-ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)), um den Namen der Datei anzugeben, wie er auf einer Plattform unterstützt wird, die das lange Dateiformat behandelt. Beide Eigenschaften sind optional. Wenn Sie jedoch **PR_ATTACH_LONG_FILENAME** festlegen, legen Sie auch **PR_ATTACH_FILENAME** fest. 
    
7. Legen Sie **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) fest, um den Namen für die Anlage anzugeben, die in einem Dialogfeld angezeigt werden kann. PR_DISPLAY_NAME ist optional. 
    
## <a name="set-pr_attach_data_bin"></a>Festlegen von PR_ATTACH_DATA_BIN
  
1. Rufen Sie [IMAPIProp::OpenProperty](imapiprop-openproperty.md) auf, um die Eigenschaft mit der **IStream-Schnittstelle** zu öffnen. 
    
2. Wenn eine Datei die Daten enthält und geöffnet ist oder Sie explizite Kontrolle über die Puffergröße benötigen, rufen Sie **IStream::Write** in einer Schleife auf, um die Daten im Datenstrom zu platzieren. 
    
3. Eine weitere Möglichkeit besteht darin, **OpenStreamOnFile** aufzurufen, um einen Datenstrom für den Zugriff auf die Datendatei zu erstellen, und dann die **IStream::CopyTo-Methode** dieses Datenstroms aufzurufen, um die Daten in den von **OpenProperty** zurückgegebenen Datenstrom zu kopieren.
    
4. Rufen Sie die **IStream::Commit-Methode** des neuen Datenstroms auf. 
    
## <a name="set-pr_attach_data_obj"></a>Festlegen PR_ATTACH_DATA_OBJ
  
1. Rufen Sie **IMAPIProp::OpenProperty** auf, um die Eigenschaft mit der **IStreamDocfile-Schnittstelle** zu öffnen, um einen Stream zu erstellen, der mit strukturiertem Speicher funktioniert. **IStreamDocfile** wird von Nachrichtenspeicheranbietern implementiert, um Clients eine leistungsstärkere Möglichkeit zum Speichern und Abrufen von strukturiertem Speicher zu bieten. Die **IStreamDocfile-Schnittstelle** ist identisch mit **IStream,** aber der Inhalt des Datenstroms wird garantiert als strukturierter Speicher formatiert. Wenn dieser Aufruf erfolgreich ist, erstellen Sie den Datenstrom mit den gleichen Schritten, die zum Festlegen **PR_ATTACH_DATA_BIN** beschrieben sind.
    
2. Wenn **OpenProperty** fehlschlägt: 
    
   1. Rufen Sie **OpenProperty** erneut auf, und fordern Sie **IStorage** an. 
      
   2. Rufen Sie **StgOpenStorage** auf, um das OLE-Objekt zu öffnen und ein Speicherobjekt zurückzugeben. 
      
   3. Rufen Sie die **IStorage::CopyTo-Methode** des zurückgegebenen Speicherobjekts auf, um in das von **OpenProperty** zurückgegebene Speicherobjekt zu kopieren.
      
   4. Rufen Sie die **IStorage::Commit-Methode** des neuen Speicherobjekts auf. 
    
## <a name="set-pr_attach_pathname"></a>Festlegen von PR_ATTACH_PATHNAME
  
1. Weisen Sie eine [SPropValue-Struktur](spropvalue.md) zu, indem Sie das **ulPropTag-Element** auf **PR_ATTACH_PATHNAME** und das **Value.LPSZ-Element** auf die Zeichenfolge festlegen, die den Dateinamen darstellt. 
    
2. Rufen Sie die [IMAPIProp::SetProps-Methode](imapiprop-setprops.md) der Anlage auf. 
    
> [!NOTE]
> Wenn Ihre Plattform lange Dateinamen unterstützt, legen **Sie sowohl PR_ATTACH_PATHNAME** als auch **PR_ATTACH_LONG_PATHNAME** fest. Es kann erforderlich sein, einen Betriebssystemaufruf durchzuführen, um den kurzen Dateinamen abzurufen. 
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Anlagen](mapi-attachments.md)

