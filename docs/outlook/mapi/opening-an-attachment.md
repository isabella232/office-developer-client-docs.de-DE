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
  
Beim Öffnen einer Anlage werden die Daten angezeigt. Wenn beispielsweise eine Dateianlage geöffnet wird, wird der Inhalt der Datei angezeigt. Während Nachrichten und Ordner mit ihren Eintragsbezeichnern geöffnet werden, werden Anlagen mithilfe ihrer **Anlagennummern** geöffnet– PR_ATTACH_NUM Eigenschaften. Weitere Informationen finden Sie **unter PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)). Anlagennummern sind über die Anlagentabelle einer Nachricht verfügbar.
  
### <a name="to-open-all-attachments-in-a-message"></a>So öffnen Sie alle Anlagen in einer Nachricht
  
1. Rufen Sie die [IMessage::GetAttachmentTable-Methode der](imessage-getattachmenttable.md) Nachricht auf, um auf die Anlagentabelle zu zugreifen. 
    
2. Rufen [Sie HrQueryAllRows auf,](hrqueryallrows.md) um alle Zeilen in der Tabelle abzurufen. 
    
3. Für jede Zeile: 
    
    1. Öffnen Sie die Anlage, indem Sie die in der Spalte **PR_ATTACH_NUM** dargestellte Anlagennummer in einem Aufruf der **IMessage::OpenAttach-Methode der** Nachricht übergeben. Weitere Informationen finden Sie unter [IMessage::OpenAttach](imessage-openattach.md). **OpenAttach** gibt einen Zeiger auf eine **IAttach-Implementierung** zurück, die Zugriff auf Anlageneigenschaften bietet. 
        
    2. Rufen Sie die **IMAPIProp::GetProps-Methode** der Anlage auf, um die **PR_ATTACH_METHOD** abzurufen. Weitere Informationen finden Sie unter [IMAPIProp::GetProps](imapiprop-getprops.md) and **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)).
        
    3. Wenn **PR_ATTACH_METHOD** auf ATTACH_BY_REF_ONLY festgelegt ist, rufen Sie **IMAPIProp::GetProps** auf, um die **PR_ATTACH_PATHNAME** abzurufen. Weitere Informationen finden Sie **unter PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)).
        
    4. Wenn **pr \_ ATTACH_METHOD** auf ATTACH BY_VALUE festgelegt ist, rufen Sie \_ **IMAPIProp::OpenProperty** auf, um die **\_ PR-ATTACH_DATA_BIN-Eigenschaft** mit der **IStream-Schnittstelle zu** öffnen. Weitere Informationen finden Sie im Beispielcode nach diesem Verfahren. Weitere Informationen finden Sie unter [IMAPIProp::OpenProperty](imapiprop-openproperty.md) und **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)).
        
    5. Wenn **PR_ATTACH_METHOD** auf "ATTACH_OLE" festgelegt ist und die Anlage ein OLE 2-Objekt ist: 
        
        1. Rufen **Sie IMAPIProp::OpenProperty auf,** um die **\_ PR-ATTACH_DATA_OBJ** mit der **IStreamDocfile-Schnittstelle zu** öffnen. Versuchen Sie, diese Schnittstelle zu verwenden, da es sich um eine Implementierung von **IStream handelt,** die garantiert mit strukturiertem Speicher mit dem geringsten Aufwand arbeitet. Weitere Informationen finden Sie **unter PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)).
            
        2. Wenn beim **OpenProperty-Aufruf** ein Fehler auftritt, rufen Sie ihn erneut auf, um die **PR_ATTACH_DATA_BIN** mit der **IStreamDocfile-Schnittstelle abzurufen.** 
            
        3. Wenn bei diesem zweiten **OpenProperty-Aufruf** ein Fehler auftritt, versuchen Sie **erneut, OpenProperty zum** Abrufen von **PR_ATTACH_DATA_OBJ.** Geben Sie jedoch die **IStorage-Schnittstelle** an, anstatt **IStreamDocfile** anzugeben. 
    
4. Wenn **PR_ATTACH_METHOD** auf ATTACH_EMBEDDED_MSG festgelegt ist, ist es nicht ungewöhnlich, dass der Wert von **PR_ATTACH_DATA_OBJ** fehler enthält. Dies liegt daran, dass Sie und der Tabellen implementier keine Möglichkeit haben, sich auf den Typ des zurückzukehrende Objekts zu einigen. Öffnen Sie die Anlage mithilfe von **IMessage::OpenAttach,** um einen Zeiger auf die angefügte Nachricht abzurufen. Greifen Sie dann auf die Anlagendaten zu, indem Sie die **IMAPIProp::OpenProperty-Methode** aufrufen. Weitere Informationen finden Sie unter [IMessage::OpenAttach](imessage-openattach.md) und [IMAPIProp::OpenProperty](imapiprop-openproperty.md).
    
Sie können anfordern, dass eine Anlage im Lese-/Schreib- oder schreibgeschützten Modus geöffnet wird. Schreibgeschützt ist der Standardmodus, und viele Nachrichtenspeicheranbieter öffnen alle Anlagen in diesem Modus, unabhängig davon, welche Clients anfordern. Übergeben Sie das MAPI_BEST_ACCESS-Flag, um zu fordern, dass der Nachrichtenspeicheranbieter die höchste Zugriffsebene gewährt, die er hat, und ruft dann die **PR_ACCESS_LEVEL-Eigenschaft** der geöffneten Anlage ab, um die tatsächlich gewährte Zugriffsebene zu bestimmen. Weitere Informationen finden Sie **unter PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).
  
Das folgende Beispiel zeigt, wie Sie die Daten in der PR-ATTACH_DATA_BIN einer **\_ Anlage** öffnen. Es weist zwei Datenströmen Zeiger zu: einen für die Datei und einen für die Anlage. Die **OpenStreamOnFile-Funktion** öffnet den Dateidatenstrom im schreibgeschützten Modus. Der Aufruf der **IMAPIProp::OpenProperty-Methode** der Anlage öffnet den Anlagendatenstrom im Lese-/Schreibmodus. Weitere Informationen finden Sie **unter PR_ATTACH_DATA_BIN**, [OpenStreamOnFile](openstreamonfile.md)und [IMAPIProp::OpenProperty](imapiprop-openproperty.md). Der Code kopiert dann aus dem Dateidatenstrom in den Anlagendatenstrom und gibt beide Datenströme frei.
  
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


