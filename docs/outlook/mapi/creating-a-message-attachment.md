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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332942"
---
# <a name="creating-a-message-attachment"></a>Erstellen einer Nachrichtenanlage
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bei einer Nachrichtenanlage handelt es sich um zusätzliche Daten wie eine Datei, eine andere Nachricht oder ein OLE-Objekt, die Sie zusammen mit einer Nachricht senden oder speichern können. Jede Anlage verfügt über eine Auflistung von Eigenschaften, die Sie identifiziert und ihren Typ und ihre Darstellung beschreibt. Wie Empfänger kann nur auf Nachrichtenanlagen über die Nachricht zugegriffen werden, zu der Sie gehören. Damit eine Anlage verwendet werden kann, muss daher Ihre Nachricht geöffnet sein.
  
## <a name="create-a-message-attachment"></a>Erstellen einer Nachrichtenanlage
  
1. Rufen Sie die [IMessage:: createattach](imessage-createattach.md) -Methode der Nachricht auf, und führen Sie NULL als Schnittstellenbezeichner aus. **Createattach** gibt eine Zahl zurück, die die neue Anlage in der Nachricht eindeutig identifiziert. Die Anlagennummer wird in der **PR_ATTACH_NUM** ([pidtagattachnumber (](pidtagattachnumber-canonical-property.md))-Eigenschaft gespeichert und ist nur gültig, solange die Nachricht, die die Anlage enthält, geöffnet ist.
    
2. Rufen Sie [IMAPIProp::](imapiprop-setprops.md) SetProps auf, um **PR_ATTACH_METHOD** ([pidtagattachmethod (](pidtagattachmethod-canonical-property.md)) festzulegen, um anzugeben, wie auf die Anlage zugegriffen wird. **PR_ATTACH_METHOD** ist erforderlich. Legen Sie den folgenden Wert fest: 
    
   - ATTACH_BY_VALUE, wenn die Anlage Binärdaten ist.
    
   - ATTACH_BY_REFERENCE, ATTACH_BY_REF_RESOLVE oder ATTACH_BY_REF_ONLY, wenn es sich bei der Anlage um eine Datei handelt.
    
   - ATTACH_EMBEDDED_MSG, wenn die Anlage eine Nachricht ist.
    
   - ATTACH_OLE, wenn die Anlage ein OLE-Objekt ist.
    
3. Legen Sie die entsprechende Eigenschaft für Anlagendaten fest:
    
   - **PR_ATTACH_DATA_BIN** ([Pidtagattachdatabinary (](pidtagattachdatabinary-canonical-property.md)) für binäre Daten und OLE 1-Objekte.
    
   - **PR_ATTACH_PATHNAME** ([Pidtagattachpathname (](pidtagattachpathname-canonical-property.md)) für Dateien.
    
   - **PR_ATTACH_DATA_OBJ** ([Pidtagattachdataobject (](pidtagattachdataobject-canonical-property.md)) für Nachrichten und OLE 2-Objekte.
    
4. Legen Sie **PR_ATTACH_RENDERING** ([pidtagattachrendering (](pidtagattachrendering-canonical-property.md)) fest, um die grafische Darstellung der Anlage für Datei-oder Binäranlagen beizubehalten. Legen Sie Sie nicht für OLE-Objekte fest, die die Renderinginformationen intern oder für angefügte Nachrichten speichern. 
    
5. Legen Sie **PR_RENDERING_POSITION** ([pidtagrenderingposition (](pidtagrenderingposition-canonical-property.md)) fest, um anzugeben, wo die Anlage angezeigt werden soll. **PR_RENDERING_POSITION** gilt nur für Clients, die die **PR_BODY** -Eigenschaft festlegen. Wenn Sie **PR_RTF_COMPRESSED**nur unterstützen, fügen Sie die folgenden Platzhalterinformationen in den komprimierten Stream ein:
    
   `\objattph`

   Um **PR_RENDERING_POSITION**festzulegen, weisen Sie eine Zahl, die einen ordinalen Offset in Zeichen darstellt, wobei das erste Zeichen von **PR_BODY** 0 ist, wenn Sie wissen möchten, wo in der Nachricht die Anlage gerendert wird, oder 0xFFFFFFFF, wenn Sie nicht Render Attachments in **PR_BODY**.
    
6. Legen Sie **PR_ATTACH_FILENAME** ([pidtagattachfilename (](pidtagattachfilename-canonical-property.md)) fest, um den Kurznamen der Datei für eine Dateianlage und eine **PR\_-ATTACH_LONG_FILENAME** ([pidtagattachlongfilename (](pidtagattachlongfilename-canonical-property.md)) anzugeben, um den Namen der unterstützten Datei anzugeben. auf einer Plattform, die das Format für lange Dateinamen verarbeitet. Beide Eigenschaften sind optional. Wenn Sie jedoch **PR_ATTACH_LONG_FILENAME**festlegen, legen Sie auch **PR_ATTACH_FILENAME**fest. 
    
7. Legen Sie **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) fest, um den Namen für die Anlage anzugeben, die in einem Dialogfeld angezeigt werden kann. PR_DISPLAY_NAME ist optional. 
    
## <a name="set-prattachdatabin"></a>PR_ATTACH_DATA_BIN festlegen
  
1. Rufen Sie [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) auf, um die Eigenschaft mit der **IStream** -Schnittstelle zu öffnen. 
    
2. Wenn eine Datei die Daten enthält und Sie geöffnet ist oder wenn Sie eine explizite Kontrolle über die Puffergröße benötigen, rufen Sie **IStream:: Write** in einer Schleife auf, um die Daten im Stream zu platzieren. 
    
3. Eine weitere Möglichkeit besteht darin, **OpenStreamOnFile** aufzurufen, um einen Stream für den Zugriff auf die Datendatei zu erstellen und dann die **IStream:: CopyTo** -Methode dieses Streams aufzurufen, um die Daten in den von **OpenProperty**zurückgegebenen Stream zu kopieren.
    
4. Rufen Sie die **IStream:: Commit** -Methode des neuen Streams auf. 
    
## <a name="set-prattachdataobj"></a>PR_ATTACH_DATA_OBJ festlegen
  
1. Rufen Sie **IMAPIProp:: OpenProperty** auf, um die Eigenschaft mit der **IStreamDocfile** -Schnittstelle zu öffnen, um einen Datenstrom zu erstellen, der mit strukturiertem Speicher funktioniert. **IStreamDocfile** wird von Nachrichtenspeicher Anbietern implementiert, um Clients eine leistungsstärkere Methode zum Speichern und Abrufen strukturierter Speicher bereitzustellen. Die **IStreamDocfile** -Schnittstelle ist mit **IStream**identisch, aber der Inhalt des Streams wird garantiert als strukturierter Speicher formatiert. Wenn dieser Aufruf erfolgreich ist, erstellen Sie den Stream mit den gleichen Schritten zum Festlegen von **PR_ATTACH_DATA_BIN**.
    
2. Wenn **OpenProperty** fehlschlägt: 
    
   1. Rufen **** Sie OpenProperty erneut an, um **IStorage**zu Fragen. 
      
   2. Rufen Sie **StgOpenStorage** auf, um das OLE-Objekt zu öffnen und ein Storage-Objekt zurückzugeben. 
      
   3. Rufen Sie die **IStorage:: CopyTo** -Methode des zurückgegebenen Speicherobjekts auf, um das von **OpenProperty**zurückgegebene Speicherobjekt zu kopieren.
      
   4. Rufen Sie die **IStorage:: Commit** -Methode des neuen Speicherobjekts auf. 
    
## <a name="set-prattachpathname"></a>PR_ATTACH_PATHNAME festlegen
  
1. Reservieren Sie eine [SPropValue](spropvalue.md) -Struktur, indem Sie das **ulPropTag** -Element auf **PR_ATTACH_PATHNAME** und den **Wert. LPSZ** -Member auf die Zeichenfolge festlegen, die den Dateinamen darstellt. 
    
2. Rufen Sie die [IMAPIProp::](imapiprop-setprops.md) SetProps-Methode der Anlage auf. 
    
> [!NOTE]
> Wenn Ihre Plattform lange Dateinamen unterstützt, legen Sie sowohl **PR_ATTACH_PATHNAME** als auch **PR_ATTACH_LONG_PATHNAME**fest. Möglicherweise müssen Sie einen Betriebssystemaufruf ausführen, um den kurzen Dateinamen abzurufen. 
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Anlagen](mapi-attachments.md)

