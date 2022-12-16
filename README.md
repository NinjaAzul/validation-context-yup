# validation-context-yup

```
  const { handleSubmit, control, setValue, watch, errors, register } = useForm({
    validationSchema: schema,
    validationContext: {
      hasAgencyDigit,
    },
  })
  
  ```
  
  
 # schema exmaple
 
 
 ```
 accountDigit: yup.when('$hasAgencyDigit', {
    is: true,
    then: yup
      .string()
      .trim()
      .required(required),
  }),
```

```
  .when('phoneType', phoneType =>
              phoneType === PHONE_TYPES.MOBILE
                ? yup
                    .string()
                    .trim()
                    .test(
                      'len',
                      'Este tipo de telefone precisa possuir DDD e o 9º dígito.',
                      val => clearNumber(val)?.length === 11,
                    )

```
