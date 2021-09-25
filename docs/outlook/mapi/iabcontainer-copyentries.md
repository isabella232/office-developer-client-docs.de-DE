---
title: IABContainerCopyEntries
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IABContainer.CopyEntries
api_type:
- COM
ms.assetid: 4e775228-5ceb-4002-9b68-999fb5889b86
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c0969e7518d2e326a35c2e37d8c94c3f6e97da27
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59580062"
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
  
> [in] Das Handle für das übergeordnete Fenster aller Dialogfelder oder Fenster, die von dieser Methode angezeigt werden. Der  _ulUIParam-Parameter_ muss Null sein, wenn das AB_NO_DIALOG-Flag im  _ulFlags-Parameter_ festgelegt ist. 
    
 _lpProgress_
  
> [in] Ein Zeiger auf ein Statusobjekt, das eine Statusanzeige anzeigt, oder NULL. Wenn  _lpProgress_ NULL ist, sollte eine Statusanzeige mithilfe des von mapi über die [IMAPISupport::D oProgressDialog-Methode](imapisupport-doprogressdialog.md) bereitgestellten Statusobjekts angezeigt werden. Der  _parameter lpProgress_ wird ignoriert, wenn das flag AB_NO_DIALOG in  _ulFlags_ festgelegt ist.
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie der Kopiervorgang ausgeführt wird. Die folgenden Flags können festgelegt werden:
    
AB_NO_DIALOG 
  
> Unterdrückt die Anzeige einer Statusanzeige. Wenn dieses Kennzeichen nicht festgelegt ist, wird eine Statusanzeige angezeigt.
    
CREATE_CHECK_DUP_LOOSE 
  
> Gibt an, dass eine lose Ebene der Duplikatprüfung durchgeführt werden soll. Die Implementierung der Prüfung auf lose duplizierte Einträge ist anbieterspezifisch. Beispielsweise kann ein Anbieter eine lose Übereinstimmung als zwei Einträge mit demselben Anzeigenamen definieren.
    
CREATE_CHECK_DUP_STRICT 
  
> Gibt an, dass eine strenge Stufe der Überprüfung doppelter Einträge durchgeführt werden soll. Die Implementierung der strengen Doppelten Eintragsüberprüfung ist anbieterspezifisch. Beispielsweise kann ein Anbieter eine strenge Übereinstimmung als zwei Einträge definieren, die sowohl denselben Anzeigenamen als auch die gleiche Messagingadresse aufweisen.
    
CREATE_REPLACE 
  
> Gibt an, dass ein neuer Eintrag einen vorhandenen eintrag ersetzen soll, wenn festgestellt wird, dass die beiden Duplikate sind.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Kopiervorgang war erfolgreich.
    
MAPI_W_PARTIAL_COMPLETION 
  
> Der Kopiervorgang war insgesamt erfolgreich, aber mindestens einer der Einträge konnte nicht kopiert werden. Wenn dieser Wert zurückgegeben wird, sollte der Aufruf als erfolgreich behandelt werden. Um diesen Wert zu testen, verwenden Sie das **makro HR_FAILED.** Weitere Informationen finden Sie unter [Verwenden von Makros für die Fehlerbehandlung.](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IABContainer::CopyEntries-Methode** kopiert Einträge aus demselben Container oder einem anderen Container. Ein Aufruf von **CopyEntries** entspricht funktional dem Ausführen der folgenden Aufrufe für jeden zu kopierenden Eintrag: 
  
1. Die [IABContainer::CreateEntry-Methode](iabcontainer-createentry.md) zum Erstellen des neuen Eintrags. 
    
2. Die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) zum Lesen von Eigenschaften aus dem zu kopierenden Eintrag. 
    
3. Die [IMAPIProp::SetProps-Methode](imapiprop-setprops.md) zum Schreiben von Eigenschaften in den neuen Eintrag. 
    
4. Die [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) des neuen Eintrags zum Speichern. 
    
5. Die [IUnknown::Release-Methode](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) des neuen Eintrags, um den Containerverweis freizugeben. 
    
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Alle Container, die die **IABContainer::CopyEntries-Methode** unterstützen, müssen modifizierbar sein. Legen Sie die AB_MODIFIABLE-Kennzeichnung Ihres Containers in der **eigenschaft PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) fest, um anzugeben, dass sie modifizierbar ist. 
  
Sie müssen alle Flags unterstützen. Die Interpretation und Verwendung dieser Flags ist jedoch implementierungsspezifisch, d. h., Sie können bestimmen, was die Semantik der CREATE_CHECK_DUP_LOOSE und CREATE_CHECK_DUP_STRICT Flags im Kontext Ihrer Implementierung bedeuten. Wenn Sie nicht ermitteln können oder nicht, ob es sich bei einem Eintrag um ein Duplikat handelt, lassen Sie immer zu, dass der Eintrag kopiert wird. 
  
Wenn das flag CREATE_REPLACE festgelegt ist, kopieren Sie den Eintrag immer, unabhängig davon, ob CREATE_CHECK_DUP_LOOSE oder CREATE_CHECK_DUP_STRICT festgelegt ist und ob der Eintrag ein Duplikat ist. 
  
Wenn CREATE_REPLACE nicht festgelegt ist und CREATE_CHECK_DUP_STRICT festgelegt ist, suchen Sie nach Duplikaten. Wenn ein Eintrag als Duplikat ermittelt wird, kopieren Sie den Eintrag nicht. 
  
Sie müssen CREATE_REPLACE nicht unterstützen. wenn CREATE_REPLACE nicht unterstützt wird, bedeutet dies, dass Sie sie problemlos ignorieren und immer eine Kopie ausführen können. 
  
Geben Sie die Warnung nur zurück, MAPI_W_PARTIAL_COMPLETION, wenn ein nicht lizenzierter Eintrag nicht kopiert werden kann. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Verwenden Sie die Flags CREATE_CHECK_DUP_LOOSE und CREATE_CHECK_DUP_STRICT, um dem Anbieter anzugeben, wie der Container die Duplikateingabeüberprüfung durchführen soll. Wenn Sie unabhängig davon, ob es sich um ein Duplikat handelt, einen Eintrag hinzufügen müssen, legen Sie keine dieser Flags fest oder legen Sie das CREATE_REPLACE Flag fest. CREATE_REPLACE gibt an, dass es Ihnen egal ist, ob ein Eintrag ein Duplikat ist; Sie möchten immer, dass er den ursprünglichen Eintrag ersetzt. 
  
## <a name="see-also"></a>Siehe auch



[ENTRYLIST](entrylist.md)
  
[IABContainer::CreateEntry](iabcontainer-createentry.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)

