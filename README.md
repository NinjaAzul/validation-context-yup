# validation-context-yup

``
  const { handleSubmit, control, setValue, watch, errors, register } = useForm({
    validationSchema: schema,
    validationContext: {
      hasAgencyDigit,
    },
  })
  
  
  
  
 # schema exmaple
 
 accountDigit: yup.when('$hasAgencyDigit', {
    is: true,
    then: yup
      .string()
      .trim()
      .required(required),
  }),
`` 
