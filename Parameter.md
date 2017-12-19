# 'Parameters'

- first citizen class
- must be serializable

## Types: 

### CFParameter

#### Operations

Method *CheckClass* Virtual added for Fixed Size parameter support
 
Method *GetCFContext* Returns a pointer to the owner CFContext
 
Method *GetClassID* Returns the Class Identifier for this object
 
Method *GetID* Returns the Identifier for this object

<hr/>
Method GetMemoryOccupation Returns the size taken by this object and its data in memory. 

#### Owner

Method *GetOwner* Gets the owner of the output parameter
 
Virtual *Method* SetOwner Sets the owner of the output parameter

#### Parameter Type 

Method *GetGUID* Gets the GUID of the parameter type.
 
Method *GetParameterClassID* Gets the Class ID of the parameter type.
 
Method *GetType* Gets the parameter type.
 
Method *IsCompatibleWith* Checks whether given parameter is compatible with current parameter type.
 
Method *SetType*  Changes the parameter type.

#### IO

Virtual Method *CopyValue* Copies the content of a parameter to this parameter.
 
Method *GetDataSize* Gets the size of the data stored by the parameter.
 
Virtual Method *GetReadDataPtr* Returns a pointer to the data.
 
Virtual Method *GetStringValue Gets the string representation of the parameter value.
 
Virtual Method *GetValue* Gets the value of the parameter.
 
Virtual Method *GetWriteDataPtr* Returns a pointer to the data.
 
Virtual Method *SetStringValue* Sets the value of the parameter using a string.
 
Virtual Method *SetValue* Sets the value of the parameter.

### CFParameterIn

Method *GetDirectSource Returns the direct source of the input parameter.
  
Method *GetRealSource* Returns the real source of data of the input parameter
 
Method *GetSharedSource* returns the shared source of the input parameter.
 
Method *GetType* Returns the type of the input parameter.
 
Method *GetValue* Copies the input parameter's value into the given buffer.
 
Method *SetUserDataDSL This function is the DSL binded version of CFObject::SetAppData above created at version=0x11042007 (cf. binding in Behaviors/DSLManager/DSL_ManagerBind_CK2.cpp)
 
Method *SetDirectSource* Sets the new direct source for the input parameter.
 
Method *ShareSourceWith* Shares the CFParameterIn with another one.
 



 

