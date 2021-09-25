---
title: Öffnen einer Anlage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: c0350698-5304-40cd-903d-279471f3c226
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ab54b14b9497cd9f1e1bc47bdc2c8d8783db65cd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591983"
---
# <a name="opening-an-attachment"></a>Öffnen einer Anlage

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beim Öffnen einer Anlage werden die Zugehörigen Daten angezeigt. Wenn beispielsweise eine Dateianlage geöffnet wird, wird der Inhalt der Datei angezeigt. Während Nachrichten und Ordner mit ihren Eintragsbezeichnern geöffnet werden, werden Anlagen mit ihren Anlagennummern geöffnet – **PR_ATTACH_NUM** Eigenschaften. Weitere Informationen finden Sie unter **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)). Anlagennummern sind in der Anlagentabelle einer Nachricht verfügbar.
  
### <a name="to-open-all-attachments-in-a-message"></a>So öffnen Sie alle Anlagen in einer Nachricht
  
1. Rufen Sie die [IMessage::GetAttachmentTable-Methode](imessage-getattachmenttable.md) der Nachricht auf, um auf ihre Anlagentabelle zuzugreifen. 
    
2. Rufen Sie [HrQueryAllRows](hrqueryallrows.md) auf, um alle Zeilen in der Tabelle abzurufen. 
    
3. Für jede Zeile: 
    
    1. Öffnen Sie die Anlage, indem Sie die in der **PR_ATTACH_NUM** Spalte dargestellte Anlagennummer in einem Aufruf der **IMessage::OpenAttach-Methode** der Nachricht übergeben. Weitere Informationen finden Sie unter [IMessage::OpenAttach](imessage-openattach.md). **OpenAttach** gibt einen Zeiger auf eine **IAttach-Implementierung** zurück, die Zugriff auf Anlageneigenschaften bietet. 
        
    2. Rufen Sie die **IMAPIProp::GetProps-Methode** der Anlage auf, um die **PR_ATTACH_METHOD** Eigenschaft abzurufen. Weitere Informationen finden Sie unter [IMAPIProp::GetProps](imapiprop-getprops.md) und **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)).
        
    3. Wenn **PR_ATTACH_METHOD** auf ATTACH_BY_REF_ONLY festgelegt ist, rufen **Sie IMAPIProp::GetProps** auf, um die **PR_ATTACH_PATHNAME-Eigenschaft** abzurufen. Weitere Informationen finden Sie unter **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)).
        
    4. Wenn **pr \_ ATTACH_METHOD** auf ATTACH BY_VALUE festgelegt \_ ist, rufen Sie **IMAPIProp::OpenProperty** auf, um die **\_ PR-ATTACH_DATA_BIN-Eigenschaft** mit der **IStream-Schnittstelle** zu öffnen. Weitere Informationen finden Sie im Beispielcode nach diesem Verfahren. Weitere Informationen finden Sie unter [IMAPIProp::OpenProperty](imapiprop-openproperty.md) and **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)).
        
    5. Wenn **PR_ATTACH_METHOD** auf ATTACH_OLE festgelegt ist und die Anlage ein OLE 2-Objekt ist: 
        
        1. Rufen Sie **IMAPIProp::OpenProperty** auf, um die **\_ PR-ATTACH_DATA_OBJ-Eigenschaft** mit der **IStreamDocfile-Schnittstelle** zu öffnen. Versuchen Sie, diese Schnittstelle zu verwenden, da es sich um eine Implementierung von **IStream** handelt, bei der garantiert mit strukturiertem Speicher mit dem geringsten Aufwand gearbeitet wird. Weitere Informationen finden Sie unter **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)).
            
        2. Wenn der **OpenProperty-Aufruf** fehlschlägt, rufen Sie ihn erneut auf, um die **PR_ATTACH_DATA_BIN-Eigenschaft** mit der **IStreamDocfile-Schnittstelle** abzurufen. 
            
        3. Wenn dieser zweite **OpenProperty-Aufruf** fehlschlägt, versuchen Sie **erneut, OpenProperty** aufzurufen, um **PR_ATTACH_DATA_OBJ** abzurufen. Geben Sie jedoch anstelle von **IStreamDocfile** die **IStorage-Schnittstelle an.** 
    
4. Wenn **PR_ATTACH_METHOD** auf ATTACH_EMBEDDED_MSG festgelegt ist, ist es nicht ungewöhnlich, dass der Wert von **PR_ATTACH_DATA_OBJ** einen Fehler enthält. Dies liegt daran, dass Sie und der Tabellen-Implementierer keine Möglichkeit haben, sich auf den Typ des zurückzugebenden Objekts zu einigen. Um einen Zeiger auf die angefügte Nachricht abzurufen, öffnen Sie die Anlage mithilfe von **IMessage::OpenAttach**. Greifen Sie dann auf die Anlagendaten zu, indem Sie die **IMAPIProp::OpenProperty-Methode** aufrufen. Weitere Informationen finden Sie unter [IMessage::OpenAttach](imessage-openattach.md) und [IMAPIProp::OpenProperty](imapiprop-openproperty.md).
    
Sie können anfordern, dass eine Anlage im Lese-/Schreibmodus oder schreibgeschützt geöffnet wird. Schreibgeschützt ist der Standardmodus, und viele Nachrichtenspeicheranbieter öffnen alle Anlagen in diesem Modus, unabhängig davon, welche Clients dies anfordern. Übergeben Sie das Flag MAPI_BEST_ACCESS, um anzufordern, dass der Nachrichtenspeicheranbieter die höchste Zugriffsebene gewährt, die er erteilen kann, und rufen Sie dann die **eigenschaft PR_ACCESS_LEVEL** der geöffneten Anlage ab, um die Zugriffsebene zu bestimmen, die tatsächlich gewährt wurde. Weitere Informationen finden Sie unter **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).
  
Das folgende Beispiel zeigt, wie die Daten in der **\_ PR-ATTACH_DATA_BIN-Eigenschaft** einer Anlage geöffnet werden. Es ordnet Zeiger zwei Datenströmen zu: einem für die Datei und einem für die Anlage. Die **OpenStreamOnFile-Funktion** öffnet den Dateidatenstrom im schreibgeschützten Modus. Der Aufruf der **IMAPIProp::OpenProperty-Methode** der Anlage öffnet den Anlagendatenstrom im Lese-/Schreibmodus. Weitere Informationen finden Sie unter **PR_ATTACH_DATA_BIN**, [OpenStreamOnFile](openstreamonfile.md)und [IMAPIProp::OpenProperty](imapiprop-openproperty.md). Der Code kopiert dann aus dem Dateidatenstrom in den Anlagendatenstrom und gibt beide Datenströme frei.
  
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


