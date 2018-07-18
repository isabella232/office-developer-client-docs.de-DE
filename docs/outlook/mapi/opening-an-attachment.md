---
title: Öffnen einer Anlage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c0350698-5304-40cd-903d-279471f3c226
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3875e51868e882ca454c06949347327a21a93eb9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793301"
---
# <a name="opening-an-attachment"></a>Öffnen einer Anlage

**Betrifft**: Outlook 
  
Öffnen einer Anlage umfasst, deren Daten anzeigen. Beispielsweise werden eine Dateianlage geöffnet wird, der Inhalt der Datei angezeigt. Während ihrer Eintragsbezeichner mit Nachrichten und Ordnern geöffnet sind, werden geöffnete Anlagen unter Verwendung ihrer Anlage Zahlen – **PR_ATTACH_NUM** -Eigenschaften. Weitere Informationen finden Sie unter **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)). Anlage Zahlen sind über eine Nachricht Anlagentabelle verfügbar.
  
### <a name="to-open-all-attachments-in-a-message"></a>So öffnen Sie alle Anlagen in einer Nachricht
  
1. Rufen Sie die Nachricht [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) -Methode zum Zugriff auf die Anlagentabelle. 
    
2. Rufen Sie [HrQueryAllRows](hrqueryallrows.md) , um alle Zeilen in der Tabelle abzurufen. 
    
3. Für jede Zeile: 
    
    1. Öffnen Sie die Anlage, indem Sie die Anlage Anzahl dargestellt in der Spalte **PR_ATTACH_NUM** in einem Aufruf der Nachricht **IMessage::OpenAttach** -Methode übergeben. Weitere Informationen finden Sie unter [IMessage::OpenAttach](imessage-openattach.md). **OpenAttach** gibt einen Zeiger auf eine **IAttach** -Implementierung, die Zugriff auf Eigenschaften für Dateianlage bereitstellt. 
        
    2. Rufen Sie die Anlage **IMAPIProp::GetProps** -Methode zum Abrufen der **PR_ATTACH_METHOD** -Eigenschaft. Weitere Informationen finden Sie unter [IMAPIProp::GetProps](imapiprop-getprops.md) und **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)).
        
    3. Wenn **PR_ATTACH_METHOD** auf ATTACH_BY_REF_ONLY festgelegt ist, rufen Sie **IMAPIProp::GetProps** zum Abrufen der **PR_ATTACH_PATHNAME** -Eigenschaft. Weitere Informationen finden Sie unter **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)).
        
    4. Wenn **PR\_ATTACH_METHOD** festgelegt ist, zum ANFÜGEN\_BY_VALUE, rufen Sie **IMAPIProp::OpenProperty** zum Öffnen der **PR\_ATTACH_DATA_BIN** -Eigenschaft mit der **IStream** -Schnittstelle. Finden Sie im Beispielcode für dieses Verfahrens. Weitere Informationen finden Sie unter [IMAPIProp::OpenProperty](imapiprop-openproperty.md) und **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)).
        
    5. Wenn **PR_ATTACH_METHOD** auf ATTACH_OLE festgelegt ist, und die Anlage ein OLE-2-Objekt ist: 
        
        1. Rufen Sie **IMAPIProp::OpenProperty** zum Öffnen der **PR\_ATTACH_DATA_OBJ** -Eigenschaft mit der **IStreamDocfile** -Schnittstelle. Versuchen Sie diese Schnittstelle verwendet werden, da es eine Implementierung der **IStream** strukturierten Speicher mit den geringsten Aufwand entwickelt gewährleistet ist. Weitere Informationen finden Sie unter **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)).
            
        2. Wenn der **OpenProperty** Aufruf fehlschlägt, rufen Sie sie erneut, um die **PR_ATTACH_DATA_BIN** -Eigenschaft mit der **IStreamDocfile** -Schnittstelle abrufen. 
            
        3. Wenn diese zweite **OpenProperty** Aufruf fehlschlägt, versuchen Sie es erneut **OpenProperty** zum Abrufen von **PR_ATTACH_DATA_OBJ**aufrufen. Geben Sie jedoch statt **IStreamDocfile**angeben, die **IStorage** -Schnittstelle. 
    
4. Wenn **PR_ATTACH_METHOD** auf ATTACH_EMBEDDED_MSG festgelegt ist, ist es nicht ungewöhnlich, dass der Wert der **PR_ATTACH_DATA_OBJ** enthält einen Fehler. Dies ist, da Sie und der Tabelle Implementierer keine Möglichkeit haben, stimmen für den Typ des zurückzugebenden Objekts. Rufen Sie einen Zeiger auf die angefügte Nachricht öffnen Sie die Anlage mit **IMessage::OpenAttach**. Klicken Sie dann auf die Anlagendaten durch Aufrufen der **IMAPIProp::OpenProperty** -Methode zugreifen. Weitere Informationen finden Sie unter [IMessage::OpenAttach](imessage-openattach.md) und [IMAPIProp::OpenProperty](imapiprop-openproperty.md).
    
Sie können anfordern, dass eine Anlage in Lese-/Schreibzugriff oder nur-Lese-Modus geöffnet wird. Schreibgeschützt ist des Standardmodus, und viele Anbieter Nachricht öffnen aller Anlagen in diesem Modus unabhängig davon, welche Clients anfordern. Übergeben Sie die Kennzeichen MAPI_BEST_ACCESS um anzufordern, dass der Nachricht Speicheranbieter erteilen die höchste Zugriffsebene anschließend die Anlage öffnen **PR_ACCESS_LEVEL** -Eigenschaft, um die Zugriffsebene zu ermitteln, die gewährt wurde, abrufen und kann. Weitere Informationen finden Sie unter **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).
  
Das folgende Beispiel zeigt, wie die Daten in einer Anlage geöffnet **PR\_ATTACH_DATA_BIN** Eigenschaft. Es belegt Zeiger auf zwei Datenströme: einen für die Datei und einen für die Anlage. Die Funktion **OpenStreamOnFile nicht ausgeführt werden** wird den Datei-Stream im schreibgeschützten Modus geöffnet. Der Anruf an die Anlage **IMAPIProp::OpenProperty** -Methode wird die Anlagendatenstrom im Lese-/Schreibmodus geöffnet. Weitere Informationen finden Sie unter **PR_ATTACH_DATA_BIN**, [IMAPIProp::OpenProperty](imapiprop-openproperty.md)und [OpenStreamOnFile nicht ausgeführt werden](openstreamonfile.md). Der Code und klicken Sie dann aus dem Dateistream an den Stream Anlage kopiert und beide Datenströme frei.
  
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


