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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 44a31e46c43a065c720564f2aa193913dbfd9a2e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791950"
---
# <a name="iabcontainercopyentries"></a>IABContainer::CopyEntries

  
  
**Betrifft**: Outlook 
  
Kopiert eine oder mehrere Einträge, in der Regel messaging Benutzer oder Verteilerlisten.
  
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
  
> [in] Ein Zeiger auf ein Array von [ENTRYLIST](entrylist.md) -Strukturen, die Einträge zum Kopieren von Eintragsbezeichner enthält. 
    
 _ulUIParam_
  
> [in] Das Handle für das übergeordnete Fenster für alle Dialogfelder oder Windows, die diese Methode anzeigt. Der Parameter _UlUIParam_ muss NULL sein, wenn das Flag AB_NO_DIALOG im _UlFlags_ -Parameter festgelegt ist. 
    
 _lpProgress_
  
> [in] Ein Zeiger auf ein Fortschritt-Objekt, eine Statusanzeige oder NULL anzeigt. Wenn _LpProgress_ NULL ist, sollte eine Statusanzeige mithilfe von MAPI bereitgestellt wird, über die [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) -Methode des Fortschritts-Objekts angezeigt werden. Der Parameter _LpProgress_ wird ignoriert, wenn das Flag AB_NO_DIALOG in _UlFlags_festgelegt ist.
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die steuert, wie der Kopiervorgang ausgeführt wird. Die folgenden Kennzeichen können festgelegt werden:
    
AB_NO_DIALOG 
  
> Unterdrückt die Anzeige einer Statusanzeige. Wenn dieses Flag nicht festgelegt ist, wird eine Statusanzeige angezeigt.
    
CREATE_CHECK_DUP_LOOSE 
  
> Gibt an, dass eine weit Ebene der doppelten Eintrag Überprüfung durchgeführt werden soll. Die Implementierung der weit doppelter Eintrag Überprüfung ist anbieterspezifisch. Beispielsweise kann ein Anbieter eine niedrigen Übereinstimmung definieren, wie alle zwei Einträge, die den gleichen Namen anzuzeigen.
    
CREATE_CHECK_DUP_STRICT 
  
> Gibt an, dass eine strikt doppelter Eintrag überprüfen ausgeführt werden soll. Die Implementierung der exakte doppelter Eintrag Überprüfung ist anbieterspezifisch. Ein Anbieter kann beispielsweise eine exakte Übereinstimmung definieren, wie alle zwei Einträge, die beide den gleichen Namen und die messaging-Adresse anzuzeigen.
    
CREATE_REPLACE 
  
> Gibt an, dass ein neuer Eintrag eine vorhandene ersetzen soll, wenn festgestellt wird, dass die beiden Duplikate sind.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Kopiervorgang war erfolgreich.
    
MAPI_W_PARTIAL_COMPLETION 
  
> Der Kopiervorgang insgesamt erfolgreich, aber eine oder mehrere Einträge konnte nicht kopiert werden. Wenn dieser Wert zurückgegeben wird, sollte der Anruf als erfolgreich verarbeitet. Verwenden Sie das Makro **HR_FAILED** , um für diesen Wert zu testen. Weitere Informationen finden Sie unter [Verwendung von Makros Fehlerbehandlung](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Hinweise

Die **IABContainer::CopyEntries** -Methode kopiert die Einträge aus der gleichen Container oder einen anderen Container. Ein Aufruf von **CopyEntries** entspricht der folgenden Aufrufe für jeden Eintrag kopiert werden: 
  
1. Die [IABContainer::CreateEntry](iabcontainer-createentry.md) -Methode, um den neuen Eintrag erstellen. 
    
2. Die [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode zum Lesen von Eigenschaften aus den Eintrag kopiert werden soll. 
    
3. Die [IMAPIProp::SetProps](imapiprop-setprops.md) -Methode zum Schreiben von Eigenschaften in den neuen Eintrag. 
    
4. Den neuen Eintrag [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode zu speichern. 
    
5. Den neuen Eintrag [IUnknown](http://msdn.microsoft.com/en-us/library/ms682317%28VS.85%29.aspx) -Methode, die den Container Verweis freigeben. 
    
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Alle Container, die die **IABContainer::CopyEntries** -Methode unterstützen müssen geändert werden. Festlegen des Containers AB_MODIFIABLE Flag in seiner **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))-Eigenschaft, um anzugeben, dass es geändert werden kann. 
  
Sie müssen alle Kennzeichen unterstützen. die Interpretation und die Verwendung dieser Flags Implementierung ist jedoch bestimmte – d. h., können Sie ermitteln, Bedeutung der Semantik der CREATE_CHECK_DUP_LOOSE und CREATE_CHECK_DUP_STRICT-Kennzeichen im Zusammenhang mit der Implementierung. Wenn Sie nicht oder nicht bestimmen, ob ein Eintrag vorhanden ist, immer zulassen Sie den Eintrag kopiert werden soll. 
  
Wenn das Flag CREATE_REPLACE festgelegt ist, kopieren Sie den Eintrag unabhängig davon, ob CREATE_CHECK_DUP_LOOSE oder CREATE_CHECK_DUP_STRICT festgelegt ist und ob der Eintrag ein Duplikat ist immer. 
  
Wenn CREATE_REPLACE nicht festgelegt ist und CREATE_CHECK_DUP_STRICT festgelegt ist, Duplikate überprüft. Wenn Sie ein Eintrag ermittelt wird, dass ein Duplikat ist, kopieren Sie den Eintrag nicht. 
  
Sie müssen nicht CREATE_REPLACE unterstützen. nicht unterstützt, CREATE_REPLACE bedeutet, dass Sie Sie ignorieren, und führen stets eine Kopie. 
  
Die Warnung MAPI_W_PARTIAL_COMPLETION nur zurück, wenn ein Eintrag nicht duplizierte kann nicht kopiert werden. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Verwenden Sie die Kennzeichen CREATE_CHECK_DUP_LOOSE und CREATE_CHECK_DUP_STRICT, um auf den Anbieter anzugeben, wie den Container doppelter Eintrag Überprüfung ausführen soll. Wenn Sie benötigen, einen Eintrag hinzugefügt werden, unabhängig davon, ob es sich um ein Duplikat handelt, entweder nicht legen Sie einen der folgenden Kennzeichen oder legen Sie das CREATE_REPLACE-Flag. CREATE_REPLACE gibt an, dass Sie nicht wichtig ist, wenn der Eintrag ein Duplikat ist; Möchten sie den ursprünglichen Eintrag ersetzen. 
  
## <a name="see-also"></a>Siehe auch



[ENTRYLIST](entrylist.md)
  
[IABContainer::CreateEntry](iabcontainer-createentry.md)
  
[IMAPIProgress: IUnknown](imapiprogressiunknown.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IABContainer: IMAPIContainer](iabcontainerimapicontainer.md)

