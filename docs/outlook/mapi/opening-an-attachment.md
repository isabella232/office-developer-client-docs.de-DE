---
title: Öffnen einer Anlage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c0350698-5304-40cd-903d-279471f3c226
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 39da1e02622d81cd12a2d4673b827d49bf418128
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430623"
---
# <a name="opening-an-attachment"></a>Öffnen einer Anlage

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Das Öffnen einer Anlage umfasst das Anzeigen der Daten. Wenn beispielsweise eine Dateianlage geöffnet wird, wird der Inhalt der Datei angezeigt. Während Nachrichten und Ordner mit ihren Eintrags-IDs geöffnet werden, werden Anlagen mithilfe ihrer Attachment Numbers- **PR_ATTACH_NUM** -Eigenschaften geöffnet. Weitere Informationen finden Sie unter **PR_ATTACH_NUM** ([pidtagattachnumber (](pidtagattachnumber-canonical-property.md)). Anlagennummern sind über die Attachment-Tabelle einer Nachricht verfügbar.
  
### <a name="to-open-all-attachments-in-a-message"></a>So öffnen Sie alle Anlagen in einer Nachricht
  
1. Rufen Sie die [IMessage:: GetAttachment](imessage-getattachmenttable.md) Table-Methode der Nachricht auf, um auf Ihre Anlage Tabelle zuzugreifen. 
    
2. Rufen Sie [HrQueryAllRows](hrqueryallrows.md) auf, um alle Zeilen in der Tabelle abzurufen. 
    
3. Für jede Zeile: 
    
    1. Öffnen Sie die Anlage, indem Sie die in der **PR_ATTACH_NUM** -Spalte dargestellte Anlagennummer in einem Aufruf der **IMessage:: openattach** -Methode der Nachricht übergeben. Weitere Informationen finden Sie unter [IMessage:: openattach](imessage-openattach.md). **Openattach** gibt einen Zeiger auf eine **IAttach** -Implementierung zurück, die Zugriff auf Anlageneigenschaften bietet. 
        
    2. Rufen Sie die **IMAPIProp::** GetProps-Methode der Anlage auf, um die zugehörige **PR_ATTACH_METHOD** -Eigenschaft abzurufen. Weitere Informationen finden Sie unter [IMAPIProp::](imapiprop-getprops.md) GetProps und **PR_ATTACH_METHOD** ([pidtagattachmethod (](pidtagattachmethod-canonical-property.md)).
        
    3. Wenn **PR_ATTACH_METHOD** auf ATTACH_BY_REF_ONLY festgelegt ist, rufen Sie **IMAPIProp::** GetProps auf, um die **PR_ATTACH_PATHNAME** -Eigenschaft abzurufen. Weitere Informationen finden Sie unter **PR_ATTACH_PATHNAME** ([pidtagattachpathname (](pidtagattachpathname-canonical-property.md)).
        
    4. Wenn **PR\_ATTACH_METHOD** auf Attach\_BY_VALUE festgelegt ist, rufen Sie **IMAPIProp:: OpenProperty** auf, um die **\_PR-ATTACH_DATA_BIN** -Eigenschaft mit der **IStream** -Schnittstelle zu öffnen. Sehen Sie sich den Beispielcode nach diesem Verfahren an. Weitere Informationen finden Sie unter [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) und **PR_ATTACH_DATA_BIN** ([pidtagattachdatabinary (](pidtagattachdatabinary-canonical-property.md)).
        
    5. Wenn **PR_ATTACH_METHOD** auf ATTACH_OLE festgelegt ist und die Anlage ein OLE 2-Objekt ist: 
        
        1. Rufen Sie **IMAPIProp:: OpenProperty** auf, um die **\_PR-ATTACH_DATA_OBJ** -Eigenschaft mit der **IStreamDocfile** -Schnittstelle zu öffnen. Versuchen Sie, diese Schnittstelle zu verwenden, da es sich um eine Implementierung von **IStream** handelt, die mit dem geringsten Aufwand mit strukturiertem Speicher kompatibel ist. Weitere Informationen finden Sie unter **PR_ATTACH_DATA_OBJ** ([pidtagattachdataobject (](pidtagattachdataobject-canonical-property.md)).
            
        2. Wenn der **OpenProperty** -Aufruf fehlschlägt, rufen Sie ihn erneut auf, um die **PR_ATTACH_DATA_BIN** -Eigenschaft mit der **IStreamDocfile** -Schnittstelle abzurufen. 
            
        3. Wenn dieser zweite **OpenProperty** -Aufruf fehlschlägt, versuchen Sie **** erneut, OpenProperty aufzurufen, um **PR_ATTACH_DATA_OBJ**abzurufen. Geben Sie jedoch anstelle von **IStreamDocfile**die **IStorage** -Schnittstelle an. 
    
4. Wenn **PR_ATTACH_METHOD** auf ATTACH_EMBEDDED_MSG festgelegt ist, ist es nicht ungewöhnlich, dass der Wert von **PR_ATTACH_DATA_OBJ** einen Fehler enthält. Dies liegt daran, dass Sie und die Tabellen Implementierung keine Möglichkeit haben, den Typ des zurückzugebenden Objekts zu vereinbaren. Wenn Sie einen Zeiger auf die angefügte Nachricht abrufen möchten, öffnen Sie die Anlage mit **IMessage:: openattach**. Greifen Sie dann auf die Anlagendaten zu, indem Sie die **IMAPIProp:: OpenProperty** -Methode aufrufen. Weitere Informationen finden Sie unter [IMessage:: openattach](imessage-openattach.md) und [IMAPIProp:: OpenProperty](imapiprop-openproperty.md).
    
Sie können anfordern, dass eine Anlage im Lese-/Schreibzugriff oder schreibgeschützt geöffnet wird. Schreibgeschützt ist der Standardmodus, und viele Nachrichtenspeicher Anbieter öffnen alle Anlagen in diesem Modus, unabhängig davon, welche Clients eine Anforderung stellen. Übergeben Sie das MAPI_BEST_ACCESS-Flag, um anzufordern, dass der Nachrichtenspeicher Anbieter die höchste Zugriffsebene gewährt, und rufen Sie dann die **PR_ACCESS_LEVEL** -Eigenschaft der geöffneten Anlage ab, um die Zugriffsebene zu bestimmen, die tatsächlich erteilt wurde. Weitere Informationen finden Sie unter **PR_ACCESS_LEVEL** ([pidtagaccesslevel (](pidtagaccesslevel-canonical-property.md)).
  
Das folgende Beispiel zeigt, wie Sie die Daten in der **PR\_-ATTACH_DATA_BIN** -Eigenschaft einer Anlage öffnen. Es weist Zeiger auf zwei Streams zu: einen für die Datei und einen für die Anlage. Die **OpenStreamOnFile** -Funktion öffnet den Dateistream im schreibgeschützten Modus. Der Aufruf der **IMAPIProp:: OpenProperty** -Methode der Anlage öffnet den Anlagendatenstrom im Lese-/Schreibzugriff. Weitere Informationen finden Sie unter **PR_ATTACH_DATA_BIN**, [OpenStreamOnFile](openstreamonfile.md)und [IMAPIProp:: OpenProperty](imapiprop-openproperty.md). Der Code kopiert dann vom Dateistream in den Anlagendatenstrom und gibt beide Streams frei.
  
```cpp
LPSTREAM pStreamFile, pStreamAtt;
HRESULT hr;
hr = OpenStreamOnFile (MAPIAllocateBuffer, MAPIFreeBuffer,
                       STGM_READ, "myfile.doc", NULL, &pStreamFile);
if (HR_SUCCEEDED(hr))
{
    // Open the destination stream in the attachment object
    hr = pAttach->OpenProperty (PR_ATTACH_DATA_BIN,
                                &IID_IStream,
                                0,
                                MAPI_MODIFY | MAPI_CREATE,
                                (LPUNKNOWN *)&pStreamAtt);
    if (HR_SUCCEEDED(hr))
    {
        STATSTG StatInfo;
        pStreamFile->Stat (&StatInfo, STATFLAG_NONAME);
        hResult = pStreamFile->CopyTo (pStreamAtt, StatInfo.cbSize,
                                       NULL, NULL);
        pStreamAtt->Release();
    }
    pStreamFile->Release();
}
```


