---
title: IABContainerCopyEntries
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABContainer.CopyEntries
api_type:
- COM
ms.assetid: 4e775228-5ceb-4002-9b68-999fb5889b86
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ddb730ed92db4c8d281e7c8d5d9b18bc44505598
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346396"
---
# <a name="iabcontainercopyentries"></a>IABContainer::CopyEntries

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Kopiert einen oder mehrere Einträge, in der Regel Messagingbenutzer oder Verteilerlisten.
  
```cpp
HRESULT CopyEntries(
  LPENTRYLIST lpEntries,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _lpEntries_
  
> [in] Ein Zeiger auf ein Array von [ENTRYLIST-Strukturen,](entrylist.md) das die Eintragsbezeichner der zu kopierenden Einträge enthält. 
    
 _ulUIParam_
  
> [in] Das Handle zum übergeordneten Fenster aller Dialogfelder oder Fenster, die von dieser Methode angezeigt werden. Der  _ulUIParam-Parameter_ muss null sein, wenn AB_NO_DIALOG im  _ulFlags-Parameter festgelegt_ ist. 
    
 _lpProgress_
  
> [in] Ein Zeiger auf ein Statusobjekt, das eine Statusanzeige oder NULL anzeigt. Wenn  _lpProgress_ NULL ist, sollte mithilfe des von MAPI bereitgestellten Progress-Objekts über die [IMAPISupport::D oProgressDialog-Methode](imapisupport-doprogressdialog.md) ein Fortschrittsindikator angezeigt werden. Der _lpProgress-Parameter_ wird ignoriert, wenn AB_NO_DIALOG in _ulFlags festgelegt ist._
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie der Kopiervorgang ausgeführt wird. Die folgenden Kennzeichen können festgelegt werden:
    
AB_NO_DIALOG 
  
> Unterdrückt die Anzeige eines Statusindikators. Wenn dieses Kennzeichen nicht festgelegt ist, wird eine Statusanzeige angezeigt.
    
CREATE_CHECK_DUP_LOOSE 
  
> Gibt an, dass eine lose Ebene doppelter Eingabeprüfungen durchgeführt werden soll. Die Implementierung der Überprüfung von losen doppelten Einträgen ist anbieterspezifisch. Beispielsweise kann ein Anbieter eine lose Übereinstimmung als zwei beliebige Einträge definieren, die denselben Anzeigenamen haben.
    
CREATE_CHECK_DUP_STRICT 
  
> Gibt an, dass eine strenge Stufe doppelter Eingabeprüfungen durchgeführt werden sollte. Die Implementierung einer strengen Doppelten Eintragsprüfung ist anbieterspezifisch. Ein Anbieter kann z. B. eine strikte Übereinstimmung als zwei Einträge definieren, die denselben Anzeigenamen und dieselbe Messagingadresse haben.
    
CREATE_REPLACE 
  
> Gibt an, dass ein neuer Eintrag einen vorhandenen Eintrag ersetzen soll, wenn festgestellt wird, dass es sich bei den beiden um Duplikate handelt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Kopiervorgang ist erfolgreich.
    
MAPI_W_PARTIAL_COMPLETION 
  
> Der Kopiervorgang war insgesamt erfolgreich, aber mindestens einer der Einträge konnte nicht kopiert werden. Wenn dieser Wert zurückgegeben wird, sollte der Anruf als erfolgreich behandelt werden. Verwenden Sie zum Testen dieses Werts **das HR_FAILED** Makro. Weitere Informationen finden Sie unter [Using Macros for Error Handling](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Hinweise

Die **IABContainer::CopyEntries-Methode** kopiert Einträge aus demselben Container oder einem anderen Container. Ein Aufruf von **CopyEntries** entspricht funktional den folgenden Aufrufen für jeden zu kopierenden Eintrag: 
  
1. Die [IABContainer::CreateEntry-Methode](iabcontainer-createentry.md) zum Erstellen des neuen Eintrags. 
    
2. Die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) zum Lesen von Eigenschaften aus dem zu kopierenden Eintrag. 
    
3. Die [IMAPIProp::SetProps-Methode](imapiprop-setprops.md) zum Schreiben von Eigenschaften in den neuen Eintrag. 
    
4. Die [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) des neuen Eintrags zum Ausführen eines Speichers. 
    
5. Die [IUnknown::Release-Methode](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) des neuen Eintrags, um den Containerverweis frei zu geben. 
    
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Alle Container, die die **IABContainer::CopyEntries-Methode** unterstützen, müssen veränderbar sein. Legen Sie das AB_MODIFIABLE des Containers in der **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) -Eigenschaft fest, um anzugeben, dass es veränderbar ist. 
  
Sie müssen alle Kennzeichen unterstützen. Die Interpretation und Verwendung dieser Flags ist jedoch implementierungsspezifisch, d. h. Sie können bestimmen, was die Semantik der CREATE_CHECK_DUP_LOOSE- und CREATE_CHECK_DUP_STRICT-Flags im Kontext Ihrer Implementierung bedeutet. Wenn Sie nicht ermitteln können oder nicht, ob es sich bei einem Eintrag um ein Duplikat handelt, lassen Sie immer zu, dass der Eintrag kopiert wird. 
  
Wenn das CREATE_REPLACE festgelegt ist, kopieren Sie den Eintrag immer, unabhängig davon, ob CREATE_CHECK_DUP_LOOSE oder CREATE_CHECK_DUP_STRICT festgelegt ist und ob es sich bei dem Eintrag um ein Duplikat handelt. 
  
Wenn CREATE_REPLACE nicht festgelegt und CREATE_CHECK_DUP_STRICT festgelegt ist, suchen Sie nach Duplikaten. Wenn ein Eintrag als Duplikat ermittelt wird, kopieren Sie den Eintrag nicht. 
  
Sie müssen keine CREATE_REPLACE. Keine Unterstützung CREATE_REPLACE bedeutet, dass Sie sie sicher ignorieren und immer eine Kopie ausführen können. 
  
Geben Sie die Warnung MAPI_W_PARTIAL_COMPLETION zurück, wenn ein nicht duplizierter Eintrag nicht kopiert werden kann. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Verwenden Sie die CREATE_CHECK_DUP_LOOSE und CREATE_CHECK_DUP_STRICT, um dem Anbieter anzugeben, wie der Container die Duplikateingabeprüfung durchführen soll. Wenn Sie unabhängig davon, ob es sich um ein Duplikat handelt, einen Eintrag hinzufügen müssen, legen Sie entweder keines dieser Flags fest, oder legen Sie das CREATE_REPLACE fest. CREATE_REPLACE gibt an, dass Es ihnen nicht egal ist, ob es sich bei einem Eintrag um ein Duplikat handelt. Sie möchten immer, dass er den ursprünglichen Eintrag ersetzt. 
  
## <a name="see-also"></a>Siehe auch



[ENTRYLIST](entrylist.md)
  
[IABContainer::CreateEntry](iabcontainer-createentry.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)

