---
title: Visual C++ (Access PC-Datenbank-Referenz)
TOCTitle: Visual C++
ms:assetid: 31d27968-e7bd-02fa-efad-26039bea30b8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249091(v=office.15)
ms:contentKeyID: 48544062
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1a12304cc30e9e653f1cb10343cac390395961fa
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473568"
---
# <a name="visual-c"></a><span data-ttu-id="a1f3b-102">Visual C++</span><span class="sxs-lookup"><span data-stu-id="a1f3b-102">Visual C++</span></span>


<span data-ttu-id="a1f3b-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a1f3b-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a1f3b-p101">Dies ist eine schematische Beschreibung, wie ADO-Ereignisse in Microsoft Visual C++ instanziiert werden. Ausführliche Informationen finden Sie unter [ADO-Ereignismodellbeispiel (VC++)](ado-events-model-example-vc.md).</span><span class="sxs-lookup"><span data-stu-id="a1f3b-p101">This is a schematic description of how to instantiate ADO events in Microsoft Visual C++. See [ADO Events Model Example (VC++)](ado-events-model-example-vc.md) for a complete description.</span></span>

<span data-ttu-id="a1f3b-106">Erstellen Sie Klassen, die von den Schnittstellen ConnectionEventsVt und RecordsetEventsVt in der Datei adoint.h abgeleitet sind.</span><span class="sxs-lookup"><span data-stu-id="a1f3b-106">Create classes derived from the **ConnectionEventsVt** and **RecordsetEventsVt** interfaces found in the file adoint.h.</span></span>

```cpp 
 
// BeginEventExampleVC01 
class CConnEvent : public ConnectionEventsVt 
{ 
 public: 
 STDMETHODIMP InfoMessage( 
 ADOError *pError, 
 EventStatusEnum *adStatus, 
 _ADOConnection *pConnection); 
... 
} 
 
class CRstEvent : public RecordsetEventsVt 
{ 
 public: 
 STDMETHODIMP WillChangeField( 
 LONG cFields, 
 VARIANT Fields, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset); 
... 
} 
// EndEventExampleVC01 
```

<span data-ttu-id="a1f3b-107">Implementieren Sie alle Ereignishandlermethoden in beiden Klassen.</span><span class="sxs-lookup"><span data-stu-id="a1f3b-107">Implement each of the event-handler methods in both classes.</span></span> <span data-ttu-id="a1f3b-108">Es ist ausreichend, dass jede Methode lediglich ein HRESULT S zurückgeben\_OK.</span><span class="sxs-lookup"><span data-stu-id="a1f3b-108">It is sufficient that each method merely return an HRESULT of S\_OK.</span></span> <span data-ttu-id="a1f3b-109">Wenn Sie allerdings bekannt geben, dass Ihre Ereignishandler verfügbar sind, werden sie standardmäßig kontinuierlich aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="a1f3b-109">However, when you make it known that your event handlers are available, they will be called continuously by default.</span></span> <span data-ttu-id="a1f3b-110">Stattdessen sollten möglicherweise nach dem ersten Mal keine weitere Benachrichtigung mehr angefordert werden, indem Sie **adStatus** auf **adStatusUnwantedEvent** festlegen.</span><span class="sxs-lookup"><span data-stu-id="a1f3b-110">Instead, you might want to request no further notification after the first time by setting **adStatus** to **adStatusUnwantedEvent**.</span></span>

```cpp 
 
// BeginEventExampleVC02 
STDMETHODIMP CConnEvent::ConnectComplete( 
 ADOError *pError, 
 EventStatusEnum *adStatus, 
 _ADOConnection *pConnection) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
// EndEventExampleVC02 
```

<span data-ttu-id="a1f3b-p103">Die Ereignisklassen erben von **IUnknown**, weshalb Sie auch die Methoden **QueryInterface**, **AddRef** und **Release** implementieren müssen. Implementieren Sie auch Klassenkonstruktoren und -destruktoren. Wählen Sie die Visual C++-Tools, die Ihnen am vertrautesten sind, um diesen Schritt zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="a1f3b-p103">The event classes inherit from **IUnknown**, so you must also implement the **QueryInterface**, **AddRef**, and **Release** methods. Also implement class constructors and destructors. Choose the Visual C++ tools with which you are most comfortable to simplify this part of the task.</span></span>

<span data-ttu-id="a1f3b-p104">Teilen Sie mit, dass Ihre Ereignishandler verfügbar sind, indem Sie **QueryInterface** in den [Recordset](recordset-object-ado.md)- und [Connection](connection-object-ado.md)-Objekten für die Schnittstellen **IConnectionPointContainer** und **IConnectionPoint** ausstellen. Stellen Sie anschließend **IConnectionPoint::Advise** für jede Klasse aus.</span><span class="sxs-lookup"><span data-stu-id="a1f3b-p104">Make it known that your event handlers are available by issuing **QueryInterface** on the [Recordset](recordset-object-ado.md) and [Connection](connection-object-ado.md) objects for the **IConnectionPointContainer** and **IConnectionPoint** interfaces. Then issue **IConnectionPoint::Advise** for each class.</span></span>

<span data-ttu-id="a1f3b-116">Angenommen, Sie verwenden eine boolesche Funktion, die **True** zurückgibt, wenn ein **Recordset** -Objekt erfolgreich informiert wird, dass Ereignishandler verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="a1f3b-116">For example, assume you are using a Boolean function that returns **True** if it successfully informs a **Recordset** object that you have event handlers available.</span></span>

```cpp 
 
// BeginEventExampleVC03 
HRESULT hr; 
DWORD dwEvtClass; 
IConnectionPointContainer *pCPC = NULL; 
IConnectionPoint *pCP = NULL; 
CRstEvent *pRStEvent = NULL; 
... 
_RecordsetPtr pRs; 
pRs.CreateInstance(__uuidof(Recordset)); 
pRStEvent = new CRstEvent; 
if (pRStEvent == NULL) return FALSE; 
... 
hr = pRs->QueryInterface(IID_IConnectionPointContainer, (LPVOID *)&pCPC); 
if (FAILED(hr)) return FALSE; 
hr = pCPC->FindConnectionPoint(RecordsetEvents, &pCP); 
pCPC->Release(); // Always Release now, even before checking. 
if (FAILED(hr)) return FALSE; 
hr = pCP->Advise(pRstEvent, &dwEvtClass); //Turn on event support. 
pCP->Release(); 
if (FAILED(hr)) return FALSE; 
... 
return TRUE; 
... 
// EndEventExampleVC03 
```

<span data-ttu-id="a1f3b-117">Nun sind Ereignisse für die **RecordsetEvent** -Familie aktiviert, und Ihre Methoden werden aufgerufen, wenn **Recordset** -Ereignisse auftreten.</span><span class="sxs-lookup"><span data-stu-id="a1f3b-117">At this point, events for the **RecordsetEvent** family are enabled and your methods will be called as **Recordset** events occur.</span></span>

<span data-ttu-id="a1f3b-118">Wenn später die Ereignishandler nicht mehr verfügbar sein sollen, rufen Sie den Verbindungspunkt erneut ab, und stellen Sie die **IConnectionPoint::Unadvise** -Methode aus.</span><span class="sxs-lookup"><span data-stu-id="a1f3b-118">Later, when you want to make your event handlers unavailable, get the connection point again and issue the **IConnectionPoint::Unadvise** method.</span></span>

```cpp 
 
// BeginEventExampleVC04 
... 
hr = pCP->Unadvise(dwEvtClass); //Turn off event support. 
pCP->Release(); 
if (FAILED(hr)) return FALSE; 
... 
// EndEventExampleVC04 
```

<span data-ttu-id="a1f3b-119">Sie müssen Schnittstellen freigeben und entsprechende Klassenobjekte zerstören.</span><span class="sxs-lookup"><span data-stu-id="a1f3b-119">You must release interfaces and destroy class objects as appropriate.</span></span>

<span data-ttu-id="a1f3b-120">Der folgende Code zeigt ein vollständiges Beispiel für eine **Recordset** -Ereignissenkenklasse.</span><span class="sxs-lookup"><span data-stu-id="a1f3b-120">The following code shows a complete example of a **Recordset** Event sink class.</span></span>

```vb 
 
// BeginEventExampleVC05 
#include <adoint.h> 
 
class CADORecordsetEvents : public RecordsetEventsVt 
{ 
public : 
 
 ULONG m_ulRefCount; 
 CADORecordsetEvents():m_ulRefCount(1){} 
 
 STDMETHOD(QueryInterface)(REFIID iid, LPVOID * ppvObject) 
 { 
 if (IsEqualIID(__uuidof(IUnknown), iid) || 
 IsEqualIID(__uuidof(RecordsetEventsVt), iid)) 
 { 
 *ppvObject = this; 
 return S_OK; 
 } 
 else 
 return E_NOINTERFACE; 
 } 
 
 STDMETHOD_(ULONG, AddRef)() 
 { 
 return m_ulRefCount++; 
 } 
 
 STDMETHOD_(ULONG, Release)() 
 { 
 if (--m_ulRefCount == 0) 
 { 
 delete this; 
 return 0; 
 } 
 else 
 return m_ulRefCount; 
 } 
 
 
 STDMETHOD(WillChangeField)( 
 LONG cFields, 
 VARIANT Fields, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
 STDMETHOD(FieldChangeComplete)( 
 LONG cFields, 
 VARIANT Fields, 
 ADOError *pError, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
 STDMETHOD(WillChangeRecord)( 
 EventReasonEnum adReason, 
 LONG cRecords, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
 STDMETHOD(RecordChangeComplete)( 
 EventReasonEnum adReason, 
 LONG cRecords, 
 ADOError *pError, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
 
 STDMETHOD(WillChangeRecordset)( 
 EventReasonEnum adReason, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
 
 STDMETHOD(RecordsetChangeComplete)( 
 EventReasonEnum adReason, 
 ADOError *pError, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
 
 STDMETHOD(WillMove)( 
 EventReasonEnum adReason, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
 
 STDMETHOD(MoveComplete)( 
 EventReasonEnum adReason, 
 ADOError *pError, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
 STDMETHOD(EndOfRecordset)( 
 VARIANT_BOOL *fMoreData, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
 STDMETHOD(FetchProgress)( 
 long Progress, 
 long MaxProgress, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
 
 STDMETHOD(FetchComplete)( 
 ADOError *pError, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
}; 
// EndEventExampleVC05 
```

